# Assignment 1
## Domains
1. **Vacation planning** - organizing trips (possibly with family and friends), planning schedules/local travel while considering budgets and other preferences

My family lives abroad, so vacation planning often involves coordinating across long distances. When traveling with family or friends, there is also often a need to manage different needs, interests and budgets. The logistics can sometimes be overwhelming, like booking tickets (especially trying to figure out the cheapest deals/combinations), as well as planning itineraries to make sure everyone’s preferences are considered and minimize unnecessary travel time. I’d like to make this process smoother and less stressful, especially when planning group trips.

2. **Productivity/time management** - managing heavy (student) schedules by helping with prioritization/time-blocking

Balancing academics, extracurriculars and personal commitments can feel overwhelming, and I often find it difficult to decide what to work on at any given time. I’m interested in figuring out ways to better organize my time, but spending time planning out my tasks takes away time to complete them. I'd like to make planning more structured and manageable, in order to stay on top of my tasks.

3. **Health management** - keeping track of metrics/choices related to a specific medical condition (e.g. type 1 diabetes in my case)

As a type 1 diabetic, I have to monitor blood glucose levels, insulin intake and diet closely, which sometimes feels time-consuming and disjointed across different apps and tools. There are also complications/risk factors that I wish to take practical measures to minimize/avoid, such as high cholesterol or lipohypertrophy. I’d like to find ways to make health management more seamless and integrated into daily life without being overwhelming.

4. **Fitness tracking** - keeping track of workout routines/schedule to work towards fitness goals while avoiding overtraining
5. **Music technology** - interactive audio tools for digital sound design and synthesis
6. **Cultural exchange/communication** - facilitating interactive/social learning of cultures and languages globally (inspired by the way MIT Global Languages teaches languages in a culturally relevant manner)
7. **Event planning** - coordinating logistics for student-led events, including scheduling, food restrictions, task delegation, budgeting
8. **Climate education/engagement** - teaching the general population about climate tradeoffs and motivating people to play their part through interactive media/games
9. **Education** - making learning more engaging, accessible, and effective through digital tools and interactive experiences
10. **Cooking** - creating a repository of healthy meals that fit various dietary/lifestyle needs

## Problems
### Domain 1: Vacation Planning
1. [Selected] **Coordinating group travel preferences** - balancing different priorities, interests and budgets when traveling with family/friends

When planning trips with family or friends, each person has different constraints and requests. Coordinating these often requires either long discussions, which may be frustrating/time-consuming, or one person ending up making most of the decisions, which may or may not have been agreed upon by everyone and could lead to a suboptimal outcome. A tool that helps automatically balance preferences (e.g. suggesting activities that satisfy most people, highlighting compromises or splitting into subgroups) could reduce stress and make trip-planning smoother.

This problem is widespread, especially among people who travel in groups. It seems it could be solvable (at least for larger/more famous tourist destinations) and the solution is relatively unique compared to existing services.

2. **Finding and booking affordable transport/accommodation** - identifying the cheapest combinations of options (flight/hotel/train etc.), especially international travel with multiple steps (could also factor in estimated costs of shorter-distance travel during the trip itself)

Many existing services already attempt to solve this problem, at least partially. It may be hard to do better without access to connections in the industry. Moreover, finding the optimal combination in terms of monetary cost may come at a compromise of other factors such as convenience or overall time spent traveling. In particular, trying to include costs of travel during the trip (e.g. in the city being visited) may be difficult when the rest of the itinerary is not finalized (flights/accommodation tend to be the first things people book).

3. **Optimizing itineraries** - reducing wasted time in transit and ensuring activities are well-organized geographically and chronologically

This problem can be somewhat solved by Google Maps and existing route-planning apps. It is a less unique problem than coordinating preferences. However, it may still be useful for such features to be included in an app that primarily solves problem 1.

### Domain 2: Productivity/Time Management
1. [Selected] **Prioritizing tasks in the moment** - balancing urgency vs. importance when many tasks are due

With multiple commitments with similar approaching deadlines, it can be hard to figure out the "correct" thing to do at any given moment. For example, should I prioritize an urgent but low-weightage assignment due tomorrow, a more important project due at the end of the week, a club responsibility or something else entirely (e.g. sleep)? A system that helps with tasks prioritization based on deadlines, estimated time needed and class/activity schedule would greatly reduce stress, time wasted and decision fatigue.

This is a personal pain point that is also relatable for many students. I find it interesting as a project because it’s not just scheduling but considers many factors to help make decisions. However, it may be difficult to estimate time needed for certain tasks, especially when it comes to larger-scale projects.

2. **Visualizing and breaking down priorities** - helping users break large projects into smaller steps and visualize how tasks compare in importance or urgency

Many existing task management tools already support subtasks, labels, and prioritization views; this problem is less unique compared to the challenge of real-time decision-making in problem 1. It also risks adding more overhead in planning rather than reducing it.

3. **Supporting focused work sessions** - combining time-blocking with reminders, progress tracking, and breaks to help users stay on task

There are already many apps addressing this space, from Pomodoro timers to habit trackers and app-blocking tools/timers. The main challenge for productivity is not the lack of focus-support systems; in fact, these may also end up adding extra time when completing tasks.

### Domain 3: Health Management
1. [Selected] **Meal planning for diabetics** - helping users plan meals while being mindful of carb intake and insulin dosing, while also considering broader goals for diabetes-specific complications/constraints like cholesterol or heart health

Unlike generic calorie counters, this could be tailored to type 1 diabetes needs, combining general nutritional goals with blood sugar control. It helps reduce decision fatigue around meals since there are already so many calculations and decisions involved in managing type 1 diabetes.

2. **Tracking health metrics in one place** - integrating blood glucose, insulin, food and exercise data across different apps/tools

Managing type 1 diabetes requires juggling multiple apps and even devices, which makes it harder to see the “big picture” of health. A solution that integrates these metrics could make self-management less overwhelming; however, as many of these devices or their associated apps involve company proprietary information, it is difficult to create an all-encompassing app without industry access.

3. **Minimizing injection-related risks** - keeping track of injection sites to avoid lipohypertrophy

This is a niche but important problem; however, it likely requires some method of physically tracking the exact injection sites, which may be difficult for a software project. It also requires the user to remember to track every time they do an injection or switch to a new pump infusion site, which may be difficult/troublesome.

## Stakeholders
### Selected Problem 1: Coordinating group travel preferences
1. **Organizer** - person leading trip planning, main user of the tool

This person would originally carry the responsibility/stress of collecting input, mediating disagreements, leading discussions/decision-making and booking logistics. A good solution would save them time and energy, as well as help them avoid awkward situations, clashes or taking full blame for decisions made by the tool.

However, they may feel a loss of control if the tool's output doesn't align with their visions, especially if they enjoy planning itineraries. Also, the tool may be unhelpful for smaller or less popular tourist destinations, which may cause frustration if the user expects more (or if this is one stop that is part of a longer trip that includes popular destinations).

2. **Participants** - family or friends joining the trip

They want their preferences represented fairly while being able to spend quality time together as a group. A good solution would prevent them from feeling left out or dissatsified, helping everyone to enjoy the trip.

However, they may feel pressured to conform if the tool focuses on majority choices or resent compromises they didn’t agree with.

3. **Tourism providers** - hotels, restaurants, tour operators

These organizations would generally benefit when decisions are made efficiently, as tourists with clearly pre-planned itineraries are more likely to confirm bookings and show up. The tourists may also end up being able to visit more places overall due to optimized planning. Additionally, their satisfaction levels for the trip would be increased if they don't need to stress about decision-making, which may improve reviews.

However, some tour operators that provide fixed itineraries for tour groups may lose out if more people start using the tool to customize their own trips. Also, smaller or less well-known providers may be overlooked by the tool.

### Selected Problem 2: Prioritizing tasks in the moment
1. **Task-doer** - student or professional managing their workload, main user of the tool

A good solution would reduce stress and decision fatigue for the task-doer, while improving productivity and saving energy and time.

However, the task-doer may grow to become over-reliant on the tool and feel anxious making decisions without it. Also, especially if the inputs are inaccurate, the tool may prioritize tasks wrongly and reduce efficiency/success rates.

2. **Collaborators** - classmates, project teammates, club members

If the task-doer becomes more productive overall, collaborators would benefit from more consistent contributions and overall smoother collaboration.

However, if the tool consistently prioritizes personal tasks over group ones or academic assignments over club work, collaborators might still experience bottlenecks. This may require the user to intervene and possibly change the inputs being used.

3. **Supervisors** - professors, managers, advisors

Supervisors typically expect timely, quality results from task-doers. A good solution would indirectly benefit the supervisor by reducing late or incomplete work. Also, overall improved productivity may improve the quality of work presented.

However, if the supervisor is unclear about exact deadlines, the task-doer would have to make one up or break down the task themself, which may or may not end up being an optimal result from the supervisor's perspective.

### Selected Problem 3: Meal planning for diabetics
1. **Diabetic individual** - patient managing their insulin intake/diet daily, main user of the tool

A good solution would help reduce decision fatigue while still allowing the patient some flexibility if they wish for it, significantly improving the patient's overall physical and mental health.

However, the patient may end up feeling constrained or enjoy their food less, especially if the meal plans become repetitive or they feel like they have lost some freedom (especially when eating with others).

2. **Caregivers/family** - those who cook, shop or otherwise support the diabetic person (it is possible that this person is also the main user of the tool on behalf of the patient, if patient is young/old/otherwise unable to care for themself)

Caregivers would benefit when there is a clear plan/guidance for how to "correctly" care for the patient, as well as less conflict about what to cook/buy. They also benefit from the healthy diet if they eat with the patient.

However, they may also feel constrained/burdened, or contribute to the patient's negative feelings if they themselves choose to deviate from the meal plan.

3. **Healthcare providers** - endocrinologists, dietitians

A good solution would result in patients with more consistent/accurate information on dietary habits, which means better information for the providers to enhance personalized care.

However, they may worry about patients over-relying on the tool, especially if its advice conflicts with the healthcare provider's opinion.

## Evidence
### Selected Problem 1: Coordinating group travel preferences
1. [Brits admit to wasting ‘hours’ planning holidays abroad – here’s how to save 10 per cent on your break](https://www.thesun.co.uk/travel/27368710/brits-waste-hours-planning-holiday-loveholidays): 17 hours and 22 minutes of the average two-week break is spent making plans; of 2,000 adults who've been on holiday within the past five years, 18% 'always' or 'often' struggle for inspiration when going away, while 29% frequently find themselves overwhelmed at the range of options available to them.
2. [BluKyte](https://www.blukyte.co/): BluKyte is a group travel app designed to simplify planning by combining real-time expense tracking, synchronized flight updates and collaborative itinerary suggestions with an upvote/downvote system into one platform.
3. [Frienzy](https://www.frienzy.com/): This app provides AI-powered itinerary creation, group voting and real-time communication, and the marketing focus seems to be on reducing the burden on trip organizers.
4. [Wanderlog](https://wanderlog.com/): A visual itinerary planning app which includes booking management, user-shared guides as well as a collaborative mode. However, it doesn't make decisions based on participants' personal preferences; instead it seems to be a repository of information which can be updated by anyone in the group.
5. [TripIt](https://www.tripit.com/web): This app organizes travel details (compiled by forwarding booking confirmation emails) into shareable itineraries with real-time updates. It does not seem to plan specific activities and primarily focuses on making sure you don't miss anything you've already booked.
6. [SplitWise](https://www.splitwise.com/): SplitWise is an expense tracking app for group trips and other situations like living with housemates.
7. [Vaiage: A Multi-Agent Solution to Personalized Travel Planning](https://arxiv.org/abs/2505.10922?utm_source=chatgpt.com): Recent research on LLM-driven travel planning, which seems something like an AI travel agent.
8. [r/travelhacks: Best way to plan group trip?](https://www.reddit.com/r/TravelHacks/comments/1hdh498/best_way_to_plan_group_trip/): suggestions that netizens have come up with for streamlining the process of planning group trips; these could be useful when designing the flow of the app
9. [How to Plan an Awesome Group Trip – 4 Different Options](https://jamboguides.com/how-to-plan-an-awesome-group-trip-4-different-options/): more tips for planning group trips
10. [Here’s Why I Stopped Planning Group Trips and Activities](https://hellolinda.medium.com/heres-why-i-stopped-planning-group-trips-and-activities-d626cdab1017): describes frustrations of being a trip organizer and presents the idea that if a planner decides not to do trip planning, someone else might eventually take the initiative to coordinate something

### Selected Problem 2: Prioritizing tasks in the moment
1. [Decision fatigue](https://en.wikipedia.org/wiki/Decision_fatigue): explains how making many decisions impairs cognitive self-control and persistence, reinforcing the need for support in prioritization
2. [Factors affecting ­individual task prioritisation in a workplace setting](https://pmc.ncbi.nlm.nih.gov/articles/PMC6502562/): a review showing that urgency, importance, task length, and personal experience influence how people prioritize tasks, suggesting opportunities for software assistance
3. [Decision Fatigue in ADHD](https://www.verywellmind.com/decision-fatigue-5215463): highlights that individuals with ADHD frequently experience mental exhaustion from daily decisions, even in mundane tasks; illustrtates broader relevance of task prioritization tools
4. [Helping Students with Decision Fatigue](https://saotg.com/helping-students-with-decision-fatigue/): a coaching program that emphasizes building executive function, time management, and reducing decision load for students, demonstrating non-software approaches to the same problem
5. [Trello](https://trello.com): a web-based project management application employing a Kanban-style workflow for organizing and tracking projects
6. [Notion](https://www.notion.com/): AI workspace for organizing notes/projects/tasks
7. [Todoist](https://www.todoist.com/): to-do list app with checkboxes, due dates, reminders and priority assignments
8. [SkedPal](https://www.skedpal.com/): AI calendar that turns to-do lists into a personalized time-blocked schedule
9. [What Is Task Prioritization?](https://www.monitask.com/en/business-glossary/task-prioritization): presents common task prioritization techniques and pitfalls which could be the basis for new features to hedge against such pitfalls
10. [Why We Struggle to Prioritize](https://eleganthack.com/why-we-struggle-to-prioritize/): key reasons behind why it is difficult to prioritize tasks and strategies to overcome it

### Selected Problem 3: Meal planning for diabetics
1. [Changes in Glycemic Control Among Individuals With Diabetes Who Used a Personalized Digital Nutrition Platform: Longitudinal Study](https://diabetes.jmir.org/2021/4/e32298?utm_source=chatgpt.com): a study of the Foodsmart platform, which offers personalized recipes, planning and grocery discounts, found improvements in self-reported HbA1c levels over time
2. [Personalised Nutritional Recommendations Based on Individual Post-Prandial Glycaemic Responses Improve Glycaemic Metrics and PROMs in Patients with Type 2 Diabetes: A Real-World Assessment ](https://www.mdpi.com/2072-6643/14/10/2123?utm_source=chatgpt.com): a real-world intervention with personalized nutritional advice significantly improved glycemic control and motivation in Type 2 diabetics
3. [REffects of personalized diets by prediction of glycemic responses on glycemic control and metabolic health in newly diagnosed T2DM: a randomized dietary intervention pilot trial](https://bmcmedicine.biomedcentral.com/articles/10.1186/s12916-022-02254-y?utm_source=chatgpt.com): for newly diagnosed Type 2 diabetics, personalized diets based on predicted glycemic responses led to better metabolic outcomes than standard Mediterranean-style diets
4. [MealMeter: Using Multimodal Sensing and Machine Learning for Automatically Estimating Nutrition Intake](https://arxiv.org/abs/2503.11683?utm_source=chatgpt.com): uses multimodal data (glucose sensors, heart rate sensors, motion sensors, environmental cues) to estimate macronutrient intake; shows potential for automating meal tracking for diabetics
5. [NutriGen: Personalized Meal Plan Generator Leveraging Large Language Models to Enhance Dietary and Nutritional Adherence](https://arxiv.org/abs/2502.20601?utm_source=chatgpt.com): generates plans aligned with user-defined calorie targets with high accuracy using LLMs and USDA references
6. [Simplified Meal Announcement Versus Precise Carbohydrate Counting in Adolescents With Type 1 Diabetes Using the MiniMed 780G Advanced Hybrid Closed Loop System: A Randomized Controlled Trial Comparing Glucose Control](https://diabetesjournals.org/care/article/46/3/544/148250/Simplified-Meal-Announcement-Versus-Precise?utm_source=chatgpt.com): study showing that carbohydrate counting is still useful even in the age of closed-loop insulin delivery systems
7. [Bridging the Gap in Carbohydrate Counting With a Mobile App: Needs Assessment Survey](https://www.jmir.org/2025/1/e63278?utm_source=chatgpt.com): a 39-question web-based survey (closed- and open-ended) was conducted o identify barriers in carbohydrate counting, preferred carbohydrate counting app features and current app use. Desired features that are typically not available include photo recognition, reliable nutrient values, personalized bolus calculations
8. [American Diabetes Assoc. meal plans](https://www.americandiabetessociety.org/meal-plans?utm_source=chatgpt.com): offers structured weekly diabetes-friendly plans and grocery lists (e.g. Mediterranean, low-carb, quick), demonstrating precedent for templated plans; however, these plans are static (PDF files)
9. [Diabetes Food Hub “Plan My Meals”](https://diabetesfoodhub.org/plan-my-meals?utm_source=chatgpt.com): drag-and-drop meal planner combined with recipe database allowing customization of weekly diabetic-friendly meals
10. [Carbs & Cals](https://carbsandcals.com/): dieting and calorie-counting app which includes carbohydrate information

## Features
### Selected Problem 1: Coordinating group travel preferences
1. **Idea shortlist** - trip participants can collectively add attractions/locations that they want to visit/stay at. They can choose from an existing list of popular options or suggest their own (e.g. a particular cafe they want to try).

Having an existing list simplifies the user experience/interface and suggests ideas that they may not have previously considered, while allowing them to suggest options outside this list will let them include their personal preferences.

2. **Weighted preference polling** - this could work two ways, depending on how involved participants want to be or how long the shortlist is. They could indicate how strongly they want to participate in each activity from the shortlist on a numeric scale, or they could indicate some general preferences quantitatively (e.g. average meal cost, rate how much they enjoy different categories of attractions or different cuisines).

The information gained from this poll can then be used to pick top attractions from the shortlist that suit the group, and create a preliminary draft of the itinerary.

3. **Itinerary tweaks** - the trip organizer can tweak parameters such as allowing the group to be split up for certain amounts of time/in certain subgroups or enforcing a certain budget. This will generate different drafts of the itinerary based on the participants' preferences.

This allows the organizer/participants to consider different options and choose the most suitable plan.

### Selected Problem 2: Prioritizing tasks in the moment
1. **Real-time task ranking and scheduling** - with every new task that is added/updated, the tool dynamically adjusts the priority ranking of tasks based on changing deadlines/workload, then drafts a schedule based on these rankings, with appropriate rest breaks and accounting for the user's usual schedule.

This is the main feature which allows the task-doer to see what they should be doing next and how busy they will be. It also allows them to see if it seems like they will not be able to complete some tasks in time (e.g. if they need to ask for an extension).

2. **Automatic task breakdown** - for larger assignments, the tool automatically proposes breaking down the task into shorter time blocks.

This prevents the task-doer from procrastinating it due to the overwhelming amount of work. If there are collaborators/supervisors, they will also be able to work with more even progress updates.

3. **Energy-saving mode** - allows the task-doer to request a simpler/less important task for the immediate future, if the task-doer is having low energy/focus levels. This feature would have a restricted usage frequency so as to make sure it is not abused.

This would enhance productivity/overall results by helping them to get sufficient rest, as well as making sure they don't mess up difficult/draining tasks when tired.

### Selected Problem 3: Meal planning for diabetics
1. **Meal plan generator** - the tool proposes meal plans for the week based on general preferences/cravings and activity/social schedule logged by the patient at the beginning of the week.

This is the main feature which provides a basic nutritional plan for the patient to follow/caregivers to prepare for, which will include estimates of nutritional information like carbohydrate content.

2. **Daily adaptive plan** - the patient will be notified daily to provide updates (if any), so that when the patient faces unexpected variances from the original plan or preferences, the plan can be updated accordingly while still trying to stick to nutritional goals.

This helps users feel less restricted and more motivated to work towards their goals.

3. **Dietary restriction profile** - the tool can save the patient's allergies or other dietary restrictions so as to avoid certain ingredients every week/day.

This ensures the meal plans will not include any foods that may be harmful or undesired.