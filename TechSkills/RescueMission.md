# Talk Title
Rescue mission accomplished

## Format
45 min talk

## Brainstorm
- Understand how it got to this place. What decisions made this happen.
    - good, fast, cheap: pick 2. More like always be juggling 2 but not the same 2. 
    - Tech debt is ok, but you need to pay it down eventually
- if the project fails its not your fault. It got into this place without you. you're not a savior
- Audit the current state of things
    - Database: referential integrity and why its important
    - Database: normalization vs denormalization and finding your balance (what is the use case? typical uses? reporting?)
- Delete dead code
    - Lessons learned, what I wish we would've done.
- Test coverage
    - Test the bugs! Helpful audit too
    - 100% coverage would be ideal, especially if you are not the team/developer that wrote the code
    - Timebox and focus on critical path
- Performance optimizations
- Security audit
- Stakeholder education is key!
    - Why are the issues you see a problem?
    - Why we can't add new features while this process is ongoing
    - Setting expectations
- Working local development environment
    - how long does it take to get the project running?
    - no more package hacks
    - copying staging/prod databases is not a solution
- Add error monitoring
- Look for and resolve general inconsistencies (API routes, json responses, error handling, parameter naming, column naming, etc)
- Clean up each layer (db, application, business, presentation)
    - Database
    - Models
    - Controllers
    - Views
- create a roadmap and share with stakeholders. explain each step and its purpose (in context of the values of your audience)
- what to do if you're the one advocating for the rescue mission? (stakeholders don't recognize the problem...)
- preventing future rescue missions
    - always leave the code better than when you found it
    - clearly named functions and variables
    - service objects
    - foreign keys and database constraints
    - model validations
    - tests for new functionality
    - backfill tests for existing code that you're using in new features
- Rewriting from scratch isn't always the answer (most of the time it isn't)
- Incremental refactors are important - small changes, one by one
- Important to keep track of commits, branches, database migrations and deploys
    - want to make sure you migrate necessary data before deploying the migration that drops the column
- You can't change a project's past, but you can rewrite it's future.


## Audience
Who is the audience?
This talk is intended for developers who are or have been tasked with trying to save an application that has incurred too much tech debt and is not stable. As developers, we tend to favor rewrites over fixing our mistakes. This talk is to show that greenfield development isn't always the answer and that you can incrementally improve a failing project.


## Outcomes/Conclusions
What will the audience get out of this talk? What do I want them to come
away with?
By the end of this talk, the audience will have tangible steps to take to incrementally stabilize a failing application. They will also be on the lookout for warning signs of too much tech debt, learn some times when tech debt is OK, and walk away with useful language to use when advocating to pay down the debt.


## Outline
- Intro
    - Story time! Talk about recent ag tech project with 4 unstable applications that couldn't reliably be set up in a local dev environment, be deployed, or be changed without unknown side effects
- Gain an empathetic understanding
    -  Understand how it got to this place - what decisions made this happen?
        - Good, fast, cheap: pick 2. Which 2 did your stakeholders choose too often?
        - How was tech debt incurred? And how was paying it down prioritized (or not)?
    - Audit the state of the existing system
        - Are you able to get the project running locally?
        - Version support of your language/framework/packages. When is EOL?
        - What edge case requirements does the project have? (looking at you IE support)
        - Security vulnerabilities
        - Static analysis - complexity, churn, code duplication, etc
        - Test coverage
        - Dead code
        - Error monitoring
        - Performance
        - Data model
            - Referential integrity in the database
            - Associations match foreign keys/columns?
            - Level of normalization - does it make sense?
        - General consistency
            - Look at API requests/reponses
            - Parameter naming
        - What does the deployment process look like?
- Make a plan
    - Rewrite vs incremental refactor?
        - Rewriting from scratch isn't always the answer (most of the time it isn't)
    - Create a roadmap to outline how you will approach stabilization
    - Create a well-informed, realistic estimate
    - Stakeholder education!!
        - Why are the issues found during the audit problematic?
        - Explain each part of the roadmap and its purpose (in context of the values of your audience)
        - Why we can't add new features while this process is ongoing
        - Clearly set expectations
- Get to work
    - Get a working local dev environment
    - Error monitoring
    - Performance monitoring
    - Security vulnerabilities
    - Test coverage
        - Test the bugs! Helpful audit too
        - 100% coverage would be ideal, especially if you are not the team/developer that wrote the code
        - Timebox and focus on critical path
    - Automated CI/CD
    - Choose your approach for refactoring - layered or domain-driven? 
        - We did a combo of both. 
        - Complicated, de-normalized data model so we would pick one domain, start at the database and refactor layer by layer from db through business logic to presentation layer
    - Incremental refactors are important - small changes, one by one
    - Deploy early and often. The smaller your deploys the better.
         - Deploying changes to the database are often done in two parts, especially when removing tables/columns and moving the data elsewhere
            - Deploy 1: Add new table/column. Migrate (copy!) the data from the old table/column to the new
            - Full QA
            - Deploy 2: Remove old table/column
- Lessons learned
    - Delete dead code!
    - Important to keep track of commits, branches, database migrations and deploys
        - want to make sure you migrate necessary data before deploying the migration that drops the column

- Conclusion
    - If the project fails its not your fault. It got into this place without you, you don't have to be a savior
    - Prevent future rescue missions
        - Always leave the code better than when you found it
        - Clearly named functions and variables
        - Service objects
        - Foreign keys and database constraints
        - Model validations
        - Tests for new functionality
        - Backfill tests for existing code that you're using in new features

### Outline to use for CFP
- Intro
    - Story time! Talk about recent ag tech project with 4 unstable applications that couldn't reliably be set up in a local dev environment, be deployed, or be changed without unknown side effects
- Gain an empathetic understanding
    -  Understand how it got to this place - what decisions made this happen?
    - Audit the state of the existing system
        - Will provide a comprehensive list of things to evaluate
- Make a plan
    - Rewrite vs incremental refactor?
    - Create a roadmap to outline how you will approach stabilization
    - Create a well-informed, realistic estimate
    - Stakeholder education!!
- Get to work
    - Get a working local dev environment
    - Error monitoring
    - Performance monitoring
    - Security vulnerabilities
    - Test coverage
    - Automated CI/CD
    - Choose your approach for refactoring - layered or domain-driven? 
    - Incremental refactors are important - small changes, one by one
    - Deploy early and often. The smaller your deploys the better.
- Lessons learned
    - Delete dead code!
    - Important to keep track of commits, branches, database migrations and deploys

- Conclusion
    - If the project fails its not your fault. It got into this place without you, you don't have to be a savior
    - How to prevent future rescue missions


## Description
As a consultant, I've had many clients bring me projects that were on their last legs. My most recent project was unable to run locally, could not be deployed reliably, and making a code change almost guaranteed unknown side effects. When faced with a rescue mission, developers are quick to say, "Scrap it. It's quicker to rewrite it from scratch." But most of the time that's an irresponsible choice. Many applications are currently making their stakeholders revenue and have onboarded users with data in the system. Deciding to stabilize a failing project in place is often a scary challenge, but can be a better option for many projects. By the end of this talk, the audience will have tangible steps to take to incrementally stabilize a failing application. They will also be on the lookout for warning signs of too much tech debt, learn some times when tech debt is OK, and walk away with useful language to use when advocating to pay down the debt.


## Abstract
"Your mission, should you choose to accept it..." A stakeholder has brought you a failing project and wants you to save it.

Do you accept your mission? Do you scrap the project and rewrite it? Deciding to stabilize a failing project can be a scary challenge. By the end of this talk, you will have tangible steps to take to incrementally refactor a failing application in place. We will also be on the lookout for warning signs of too much tech debt, learn when tech debt is OK, and walk away with useful language to use when advocating to pay down the debt.


## Submitted to
- RailsConf 2020
- That Conference 2020


## Given at
- ...
