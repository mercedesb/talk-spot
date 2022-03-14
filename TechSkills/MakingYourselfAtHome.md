# Talk Title
Come on in! Making yourself at home in a new codebase

## Format
30 minutes

## Brainstorm
- run the code
- read the code!
  - trace from something you know
  - open all the files, search for method names, find all instances that something is called
- step through the code
  - interactive debugging is a wonderful tool to be able to slow down and look at the state of variables line by line
- if you are a visual learner, draw pictures or find tools that will automate that for you
  - AppMap?? (RailsConf talk)
- git history
  - check commit messages, find project management tickets
  - see if you can understand the context of the code: why was it added, who asked for it, how long ago?
  - git issues/PRs  
  - learning: good commit messages
- read the tests
  - good tests will describe expected behavior and pre/post conditions
  - they can help tell you what code is supposed to do if you are having trouble groking it from the code itself
- org docs
  - are there design docs?
  - are there Slack convos discussing approaches?
  - are there docs about previous iterations (this one is tricky if they haven't been marked as deprecated!)
- read dependency docs
  - if you are assigned a bug and can't figure out what's going on, don't be afraid to dig into documentation about dependencies or libraries the code is using
  - SSO error and hapi doc anecdote
  - SDG&E Oracle/Rails insert_all anecdote
- have empathy and compassion
  - with the previous devs
  - with yourself
- don't be afraid to make changes
  - is a variable name confusing, change it!
  - does a !(this && that) confuse you so you'd rather check (!this || !that)? do it!
- try to find examples of what you're trying to do
- mimic existing patterns
  - it might take a while to understand exactly what you're doing but reproducing existing patterns can help you learn where data is coming from and how it moves through the system
  - as you mimic more and more and then debug, you'll gradually learn where the subtle differences are and when you need to make changes
- make things reusable
- read the error messages and stack traces
- document what you're learning (commit messages, PRs, README, etc)
- make things easier for future you

## Audience
This talk is intended for devs who recently switched jobs or are experiencing anxiety about diving into a new codebase and are looking for strategies to feel more confident about conquering the unknown.


## Outcomes/Conclusions
At the end of this talk, the audience will have steps they can take in order to increase their understanding of how parts of a new codebase fit together. We'll normalize the stress and anxiety we feel when we're working with something we didn't write and we don't understand yet so that we can move past it and focus on learning. And we'll talk about what we can do to make our codebases more welcoming to guests in the future.

## Pitch
I've been a consultant for almost 10 years so I regularly need to jump into unfamiliar codebases and start contributing quickly. This can mean up to 20 new codebases a year and they're not always in tech stacks or languages that I'm familiar with. With this experience, I've learned a ton of strategies for understanding new code and figuring out how to ship code quickly. Learning how to read others' code is not a skill that's taught in most educational programs and whether someone is early in their career or switching jobs, it's a valuable skill to learn and practice.


## Outline
- I. Intro
  - My consultant experience: can work in up to 20 codebases/year
  - Anxiety in a new codebase is super normal
  - Practice makes perfect
- II. Welcome: Gaining an understanding
  - Read and reread the code: tips for how to trace functionality in the codebase
  - Interactive debugging
  - Leverage version control (Git): history, commit messages, PRs
  - Documentation!: READMEs, design docs, Slack threads, project management tickets
- III. Settling in: Making changes
  - Find existing examples and mimic
  - Be kind to yourself and others: don't be afraid to simplify
  - Error messages and stack traces
  - Documentation!: Dependencies, library documentation, code tracing of dependencies
- IV. Being a good host: make your codebase welcoming for future guests
  - Descriptive, appropriately abstracted and encapsulated code: good naming, single responsibility, simple until you need it complex
  - Good commit messages and PR descriptions: link to docs or Github issues that pointed you in the right direction, explain the _why_ and context of a change
  - Write valuable tests that describe the expected behavior
  - Documentation! (notice a pattern 😉): document what you've learned, update the docs if you found things were out of date
- V. Conclusion


## Description


## Abstract

"Welcome! We're so excited to have you 🤗 please excuse the mess." – if a codebase could talk

When we join a new team or start a new project, we have to onboard to the codebase. Diving into code that we're unfamiliar with can be stressful or make us feel like we don't know what we're doing. And the longer the codebase has been around, the more intense those feelings can be. But there are steps we can take to understand new code and start contributing quickly. In this talk, we'll cover how to build our code comprehension skills and how to make our own code welcoming to guests in the future.

## Abstract (too long)
"Welcome! We're so excited to have you 🤗 please excuse the mess." - if a codebase could talk

Whenever we join a new team or start a new project, we have to onboard to the codebase. Diving into code we didn't write and that we're unfamiliar with can be stressful and make us feel like we don't know what we're doing. And the longer the codebase has been around, the more intense those feelings can be. But there are simple, consistent steps we can take to familiarize ourselves with new code and start contributing quickly. In this talk, we'll talk about how to build our code comprehension skills and how to make our own codebases more welcoming to guests in the future.

Come on in, put your feet up. Let's get comfy.


## Submitted to
- RubyConf 2021
- RailsConf 2022
- Women Who Code Connect 2022


## Given at
- ...
