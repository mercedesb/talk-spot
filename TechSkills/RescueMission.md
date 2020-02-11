# Talk Title

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


## Audience
Who is the audience?
This talk is intended for developers who are or have been tasked with trying to right a sinking project. As developers, we tend to favor rewrites over fixing our mistakes. This talk is to show that greenfield development isn't always the answer and that you can incrementally improve a failing project.


## Outcomes/Conclusions
What will the audience get out of this talk? What do I want them to come
away with?


## Outline


## Description


## Abstract


## Submitted to
- ...


## Given at
- ...
