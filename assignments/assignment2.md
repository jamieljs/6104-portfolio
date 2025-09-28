# Assignment 2
## Problem Statement
### Problem Domain
Balancing academics, extracurriculars and personal commitments can feel overwhelming, and I often find it difficult to decide what to work on at any given time. I’m interested in figuring out ways to better organize my time; however, spending time planning out my tasks takes away time to complete them, and I often face stress deciding what to work on at any given moment (especially when multiple tasks feel equally urgent). I'd like to make planning more structured and manageable, in order to stay on top of my tasks without burning out.

### Key Problem: Prioritizing tasks in the moment

When a student has multiple competing tasks (e.g. an urgent but low-weightage assignment due tomorrow, a high-weightage project due later in the week, a club responsibility, personal rest needs), it can be overwhelming to choose the "correct" thing to do next. This leads to wasted time, stress, and sometimes poor outcomes.

The difficulty is not just in scheduling a calendar but in real-time decision-making about prioritization. A system that helps with tasks prioritization based on many factors such as deadlines, estimated time needed and class/activity schedule would greatly reduce stress, time wasted and decision fatigue.

### Stakeholders
1. **Task-doer** - student or professional managing their workload, main user of the tool
2. **Collaborators** - people affected by the task-doer's productivity on group tasks, e.g. classmates, project teammates, club members
3. **Supervisors** - people who expect timely, quality results from the task-doers, often the ones who assigned the work, e.g. professors, managers, advisors

### Evidence
1. [Decision fatigue](https://en.wikipedia.org/wiki/Decision_fatigue): explains how making many decisions impairs cognitive self-control and persistence, reinforcing the need for support in prioritization
2. [Factors affecting ­individual task prioritisation in a workplace setting](https://pmc.ncbi.nlm.nih.gov/articles/PMC6502562/): a review showing that urgency, importance, task length and personal experience influence how people prioritize tasks, highlighting the complexity of the problem which provides opportunities for software assistance
3. [Decision Fatigue in ADHD](https://www.verywellmind.com/decision-fatigue-5215463): highlights that individuals with ADHD frequently experience mental exhaustion from daily decisions, even in mundane tasks; illustrtates broader relevance of task prioritization tools
4. [What Is Task Prioritization?](https://www.monitask.com/en/business-glossary/task-prioritization): presents common task prioritization techniques and pitfalls which could be the basis for new features to hedge against such pitfalls
5. [Why We Struggle to Prioritize](https://eleganthack.com/why-we-struggle-to-prioritize/): key reasons behind why it is difficult to prioritize tasks and strategies to overcome it
6. [Helping Students with Decision Fatigue](https://saotg.com/helping-students-with-decision-fatigue/): a coaching program that emphasizes building executive function, time management, and reducing decision load for students, demonstrating non-software approaches to the same problem

### Comparables
1. [Trello](https://trello.com): a web-based project management application employing a Kanban-style workflow for organizing and tracking projects
2. [Notion](https://www.notion.com/): AI workspace for organizing notes/projects/tasks
3. [Todoist](https://www.todoist.com/): to-do list app with checkboxes, due dates, reminders and priority assignments
4. [SkedPal](https://www.skedpal.com/): AI calendar that turns to-do lists into a personalized time-blocked schedule, showing demand for smart prioritization tools


## Application Pitch
Every day, students and professionals alike are faced with the same exhausting question: *what should I work on right now?* With deadlines piling up and projects of different sizes competing for attention, choosing the “right” task can feel just as stressful as actually doing the work. NexTask is designed to take that burden off your shoulders.

At its core, NexTask helps you decide what to do next. Instead of juggling calendars, sticky notes and endless to-do lists, you open the app and see clear recommendations tailored to your deadlines, goals, and state of mind.

The first feature, **Dynamic Task Ranking**, automatically organizes your tasks in real time. As new assignments come in or deadlines change, NexTask reprioritizes them instantly. For students, this means less time wasted debating and more time actually finishing work. For supervisors and collaborators, it means steadier, more reliable progress.

The second feature, **Smart Breakdowns**, takes large, intimidating assignments and splits them into manageable pieces. Instead of staring at “Write research paper,” you’ll see smaller steps like “Draft outline for research paper” or “Write introduction,” scheduled in a logical order. This not only reduces procrastination but also ensures supervisors and collaborators see more consistent updates along the way.

Finally, NexTask includes **Energy-saving Mode**, a simple toggle that adapts your task list to your current focus and energy level. If you're feeling drained after a long day, simply switch on Energy Mode, and NexTask will suggest lighter, lower-stakes tasks for the immmediate future so you can keep moving forward without burning out. For busy students or professionals, this means better balance and fewer late nights of wasted effort.

With NexTask, the decision fatigue of constant prioritization disappears. You’ll always know what’s most important, how to start and how to keep going. Stop stressing and guessing; start doing.

## Concept Design
Design a set of concepts that will embody the functionality of your app and deliver its features. We expect you to have 3-5 concepts. Fewer than 3 concepts would probably mean limited functionality or a lack of separation of concerns; more than 5 likely suggests overambition or lack of focus. (Talk to us if you think you need more!) The deliverables are:

    The concept specifications, written in the standard form.
    Some essential synchronizations. You do not need an exhaustive collection of synchronizations, but should capture (a) any essential design ideas that involve multiple concepts; (b) representative syncs for kinds of sync that are common throughout your application (such as syncs for access control or notification).
    A brief note, at most half a page long, explaining the role that your concepts play in the context of the app as a whole. For example, if you have an authentication or authorization concept, you should say how it’s used to control access to other particular concepts. You should also explain how generic type parameters will be instantiated whenever it’s non obvious. (For example, that a generic user type will be bound to the users of an authentication concept is obvious; that the targeted items of an upvoting concept are users would not be.)

## UI Sketches
Construct some low-fidelity sketches of your user interface that show the primary user interface elements and their rough layout, annotated with pointers or comments to explain anything that might not be obvious. You should omit any error handling and standard interactions (such as user registration), but should aim to convey how the essential features appear and are used. You can use any tool you like to draw the sketches, or you can draw them by hand and scan them. You should include them in your design document as images referenced in markdown.

## User Journey
Write a narrative that follows a single stakeholder as they encounter the problem and use your designed app to address it. Tell their story in chronological order: what triggers their need, the steps they take with the app (referring to the wireframes), and the outcome. A good journey should both persuade a reader that the problem is worth solving, and illustrate how your app might help solve it. The deliverable here is a few short paragraphs that form a coherent story but identify individual steps clearly, and that reference your sketches when appropriate.