# Problem Set 1
## Exercise 1
1.
    - For each `Request`, `count` ≥ 0.
    - For each `Item`, sum of `count`s for `Purchase`s associated with this `Item` ≤ sum of the original `count`s (from `addItem`) for `Request`s associated with this `Item`

    The second invariant is more important because it prevents the friends from buying and gifting more of a certain item than the user wanted.
    
    The most affected action is `purchase`, because it is the only action that decreases the count of any `Request`. This is achieved by requiring the precondition that the given `registry` contains a `Request` for the given `item` with at least the given `count`, before the count for that `Request` can be decremented by the action.
2. `removeItem` potentially breaks this, if the action tries to remove a `Request` that has previously had its `count` decremented by some `purchase` action. The problem can be fixed by requiring that a request for the item **that does not have any `Purchase`s associated with it** exists in the registry, instead of the current precondition (i.e. don't allow `Request`s that are associated with some `Purchase`(s) to be removed)
3. Yes, reopening after a close is allowed. The gift recipient may want to temporarily close the registry while editing it.
4. In the long term, yes for data cleanup (e.g. removing old registries that have not had any actions performed in a long time).
5. Giver: which items in the are still available to purchase (i.e. `Request` has `count` ≥ 0); owner: which items have been purchased and by whom (i.e. all `Purchase`s that are associated with some `Request`)
6. Add a `hidden` flag to the `Registry` state as well as the arguments for `create`. If the recipient/registry owner wants to hide the purchases, they will set this flag to true when creating the registry; otherwise false.
7. This separates the concept of gift registration from specific catalogs of items or user groups, which allows the concept to be reused across different stores.

## Exercise 2
1./2.

**concept** PasswordAuthentication
 
**purpose** limit access to known users

**principle** after a user registers with a username and a password, they can authenticate with that same username and password and be treated each time as the same user

**state**
- a set of Users with
    - a username String
    - a password String

**actions**
- register (username: String, password: String): (user: User)
    - **requires** no existing User has this username
    - **effects** create a new User with the given username and password, and return that User
- authenticate (username: String, password: String): (user: User)
    - **requires** a User with this username and password exists
    - **effects** return the User that matches the given username and password

-----

3. Usernames must be unique. This is preserved via the precondition of `register`, which checks that there is no existing `User` with the desired `username` before creating a new `User`. `authenticate` doesn't change the state, so the invariant is preserved.
4.

new state:
- a set of PendingUsers with
    - a username String
    - a password String
    - a token String

updated `register` action:
- register (username: String, password: String): (pendingUser: PendingUser, token: String)
    - **requires** no existing User or PendingUser has this username
    - **effects** create a new secret token and a new PendingUser with the given username and password; return the PendingUser and token

new `confirm` action:
- confirm (username: String, token: String): (user: User)
    - **requires** a PendingUser with the given username and token exists
    - **effects** create a new User with the same username and password Strings as the required PendingUser, remove that PendingUser and return the new User

## Exercise 3
**concept** PersonalAccessToken
 
**purpose** allow users to authenticate to GitHub without using their password

**principle** a user generates one or more tokens, which can be scoped to limit what actions they allow, and can be deleted at any time. the user can log in to their account using token authentication instead of a password.

**state**
- a set of Tokens with
    - a value String
    - an owner User
    - a name String
    - a scopes set of Strings
    - an optional expiration Date
- a set of Users with
    - a username String
    - a password String
    - a tokens set of Tokens

**actions**
- create(user: User, name: String, scopes: String[]): (token: Token)
    - **requires** user exists and no existing token of this User has the same name
    - **effects** creates a new Token with a new secret value, the given name, owner and scopes; returns this new Token
- setExpirationDate(token: Token, expiration: Date): (token: Token)
    - **requires** token exists, expiration is after current date
    - **effects** update the expiration date of the given token to the given expiration date; return the Token
- delete(token: Token): (void)
    - **requires** token exists
    - **effects** remove token from the overall set of Tokens and from set of Tokens of user that it belongs to
- authenticate(username: String, value: String): (user: User)
    - **requires** a User with the given username exists; this User has a Token with the given value which has not yet expired
    - **effects** return the User that matches the requirements

It differs from PasswordAuthentication because there can be multiple tokens but only one password; this allows tokens to be used to control the scope of access allowed when a user is authenticated, and also allows tokens to be created/deleted without affecting other tokens (e.g. to revoke access on a particular device).

The start of the GitHub page emphasizes the similarity between tokens and passwords (that a token needs to be protected and should not be recklessly shared), but does not highlight the differences clearly. It should include something like:
> Personal access tokens are an alternative to passwords for authentication, which can be scoped to different uses/levels of access.

## Exercise 4
### URL Shortener
**concept** URLShortener

**purpose** convert long URLs into shorter aliases that are easier to share and remember, with either system-generated or user-defined suffixes

**principle** a user provides a long URL and optionally a preferred suffix. If the suffix is provided and not yet taken, the system creates a short URL that redirects to this long URL; otherwise the user is asked to provide a different suffix (or none). If the suffix is not specified, the system generates a unique suffix for the short URL that redirects to the long URL.

**state**
- a set of ShortURLs with
    - a suffix String
    - an originalURL String

**actions**
- shorten(url: String): (shortURL: ShortURL)
    - **requires** url is valid
    - **effects** generates a suffix that does not already belong to an existing ShortURL, creates a ShortURL with this suffix and the given original URL, returns the ShortURL
- shortenWithSuffix(url: String, suffix: String): (shortURL: ShortURL)
    - **requires** url is valid, suffix does not belong to any existing ShortURL
    - **effects** creates a ShortURL with the given suffix and the given original URL, returns the ShortURL
- expand(suffix: String): (url: String)
    - **requires** suffix belongs to an existing ShortURL
    - **effects** returns original URL

### Electronic Boarding Pass
**concept** ElectronicBoardingPass [User]

**purpose** enable passengers to use digital boarding passes that reflect real-time flight information updates, instead of physical paper boarding passes

**principle** a passenger opens their mobile device to present the digital boarding pass, which displays a QR code for security staff to scan in place of an ordinary boarding pass. The information displayed on the screen dynamically updates based on the airline information.

**state**
- a set of Flights with
    - a flightNumber String
    - a scheduledDeparture DateTime
    - an assignedGate String
    - a departureAirport String
    - an arrivalAirport String
- a set of BoardingPasses with
    - a passenger User
    - a flight Flight
    - a qrData String
    - a seatNumber String
    - a status String

**actions**
- issuePass(passenger: User, flight: Flight): (pass: BoardingPass)
    - **requires** given passenger has valid booking for given flight, no BoardingPass with the given passenger and flight exists
    - **effects** creates a new BoardingPass with status "issued", a generated (unique) qrData for the QR code data and an assigned seatNumber; returns this BoardingPass
- updateFlight(flight: Flight, newGate?: String, newTime?: DateTime): (newFlight: Flight)
    - **requires** flight exists in the system
    - **effects** updates assignedGate and/or scheduledDeparture time for the given flight; return the updated Flight
- checkIn(qrData: String): (void)
    - **requires** a pass with the given qrData and "issued" status exists, its corresponding flight has not departed
    - **effects** updates pass status to "checked-in"
- boardFlight(pass: BoardingPass): (void)
    - **requires** a pass with the given qrData and "checked-in" status exists, its corresponding flight has not departed
    - **effects** updates pass status to "boarded"

**notes**
- if the Flights are not stored by reference in the BoardingPasses, then the flight information updates will need to be propagated for every call to updateFlight
- does not support seat swaps/changes; if this is needed, we would need to additionally keep track of the set of available seats in each Flight
- BoardingPass status exists to prevent people from reusing boarding passes

### Time-Based One-Time Password (TOTP)
**concept** TimeBasedOTP

**purpose** strengthens security of user authentication by requiring users to provide (besides their password) a short-lived numeric token, generated from a secret shared between the user's device and the application server

**principle** a user registers for a TOTP, which causes a secret key to be generated by the application server and shared with an authenticator app on the user's device. When the user wants to log in to the application, they provide their password and the time-based token generated by the authenticator app for that particular application. The user is only authenticated if the provided password matches the password for this user in the database and the provided token matches the token calculated by the application server.

**state**
- a set of Users with
    - a username String
    - a password String
    - a totpKey String
    - a totpEnabled Boolean

**actions**
- enableTOTP(user: User): (key: String)
    - **requires** user exists and its totpEnabled is false
    - **effects** generate a new totpKey String for this user, set totpEnabled to true, return the newly generated String to be shared securely with the authenticator app
- disableTOTP(user: User): (void)
    - **requires** user exists and its totpEnabled is true
    - **effects** set the totpKey to the empty string and set totpEnabled to false
- authenticate(username: String, password: String, token: String): (user: User)
    - **requires** user with given username and password exists; either its totpEnabled is false (i.e. no further authentication happens), or its totpEnabled is true and the computed server-side token (from totpKey and current server time) matches the given token
    - **effects** return the matching user

**notes**
- TOTP provides stronger protection than password-only authentication because:
    - even if a password is leaked, an attacker cannot log in without also knowing the TOTP key (only stored in the user’s device and the server)
    - tokens are short-lived, reducing the risk of replay attacks
    - it is stronger than SMS/email codes because the attacker might be able to impersonate the user's mobile number/email address or intercept messages, thus receiving the sent token (unlike with the physical device where the token is generated using the stored key locally)
- Remaining vulnerabilities:
    - If the user's device is compromised, the TOTP key can be stolen
    - A phishing attack may still work if the attacker gets the generated token from the user with enough time to spare before it expires