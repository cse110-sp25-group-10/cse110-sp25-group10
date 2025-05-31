# Team 10x - May 22 Meeting Minutes

## Table of Contents

- [Team 10x - May 22 Meeting Minutes](#team-10x---may-22-meeting-minutes)
  - [Table of Contents](#table-of-contents)
  - [Attendance](#attendance)
  - [Meeting Agenda](#meeting-agenda)
    - [The Recording Feature](#the-recording-feature)
    - [CI/CD Pipeline](#cicd-pipeline)
  - [Talking Points](#talking-points)
    - [Sprint Review:](#sprint-review)
      - [Determining the Main Repo](#determining-the-main-repo)
      - [The Crud Functions](#the-crud-functions)
      - [The Underlying Data](#the-underlying-data)
      - [The HTML](#the-html)
      - [The CSS](#the-css)
    - [Re-Evaluating the Recording Feature.](#re-evaluating-the-recording-feature)
    - [CI/CD Pipeline](#cicd-pipeline-1)
      - [Tutorial](#tutorial)
      - [Human Review Guidelines:](#human-review-guidelines)
    - [Testing](#testing)
    - [Story Points](#story-points)
    - [Closing Remarks](#closing-remarks)
  - [TODOs:](#todos)
  - [Summary](#summary)

## Attendance

- [x] Alan Shapow
- [x] Alex Pan
- [x] Audrey Fernandez
- [x] Branden Sioson
- [x] Eric Wang
- [x] Fong Lin
- [x] Johnson Chung
- [x] Loreen Samaan
- [x] Nicholas Nurwinata
- [x] Ryan Kung
- [x] Taha Qamar

## Meeting Agenda

The larger purpose of this meeting is to evaluate the current progress on the project, and outline the next steps for the second sprint. However, there were also a few other points that needed to be discussed.

### The Recording Feature

We previously stated that users should be able to record multiple variations of a card. Nick suggests that this should be changed.

### CI/CD Pipeline

There are a few details about the CI/CD pipeline that are still unclear. These should be described in greater detail.

## Talking Points

### Sprint Review:

#### Determining the Main Repo

The Flash Card repository is now officially the main repository. It currently contains the style guides, administrative documentation, meeting minutes, etc.

#### The Crud Functions

- Each of the CRUD functions have templates
  - These define what they should do, and how they should be implemented.
  - The implementation is still pending on most.
- The Create Card function was implemented.
- Fong worked on the Shuffle and Update functions.
- Taha looked at the Read functions, but did not push yet.

#### The Underlying Data

- In Javascript, we can have data and functions bound to specific objects (think OOP).
  - We will probably use JS objects instead of using a class, because classes are *mostly* supported, but objects are **fully** supported by most browsers.
- Each card will be an object with a front text, a back text, and other various properties.
  - These can be extracted and thrown into tags and HTML components in a manner not dissimilar to the labs.
  - The renderer will combine everything in one go.
- The deck will effectively be a data structure - likely an array - that contains all of the cards objects in order.
  - To create a deck, you create a normal variaable and call the functions.
  - Every Javascript Object is formatted with key value pairs.

#### The HTML

- The majority of the underlying HTML is complete. 
- Some of it has small errors that will be addressed during styling.

#### The CSS

The CSS team did some practice work, but nothing is ready so far. This sprint, there will be work done.

### Re-Evaluating the Recording Feature.

How many recordings should the user be able to save / access per card?

- Nick spent some time prototyping the recording features, and found it difficult to work with several recordings at once.
- Our wireframe doesn't really describe how the user would access several recordings - it just gives the user the option to play back the last one.

The final verdict: The user will only be able to access **the previous recording** on any given card.

### CI/CD Pipeline

Alex gave a rundown of the CI/CD pipeline in its current iteration.

#### Tutorial

1. Begin by making a branch to work on - pushing to main directly is **blocked**.
2. The linters can be run manually while working on a branch.
   - For more information, see the README and the styleguides located in the repo.
3. Push to your remote branch.
4. Make a pull request.
    - When you open a pull request, GitHub Actions automatically runs the linters and unit tests.
    - When done, you need [Human Review](#human-review-guidelines).
    - Then, you can merge.
5. Whenever something is built to main, it builds the github pages site from index.html.
   - The TA mentioned that GitHub Pages will give us issues later, so this step may change.

*Addendum: There should be a JS Docs generator, but it is currently broken - it is set up to push to main, but this is currently blocked.*

#### Human Review Guidelines:

When making a pull-request, keep the following in mind:

- The repository is set up such that every pull request must have at least one reviewer.
- When making the pull request, please **tag individuals to be reviewers**.
  - If you're not sure who to add, try adding someone from the team associated with your pull request (CSS, Javascript, Testing, etc.)

When you are assigned as a **reviewer**, you can do the following as part of your evaluation:

- Add tests and run validators when appropriate.
- Ensure you can understand the code **at a glance**.
- Look over variable naming.


### Testing

Over the course of the meeting, various points were brought up regarding testing.

- The current priority for the testing team is to make unit tests for the basic CRUD, as this is the main focus for this sprint.
  - Make sure to go wild with esoteric combinations for inputs
- When a bug is found during testing, immediately ping someone annd make a bug issue.
- We need code coverage testing and code quality checking to be added (TA Recommendation).
- We also want integration testing to start.
- We must implement some standards for compatibility testing.

### Story Points

So far, our issue sizes have been either "small, medium, or large."

These can easily translate into **deadlines** - as clear deadlines have been a problem point in our previous sprint.

- **Small** tasks should be completed in **2 days**.
- **Medium** tasks should be completed in **4 days**.
- **Large** tasks should be completed by the **end of the sprint**.

### Closing Remarks

- If two people are working on the same branch together, communication is *key*.
  - Notify others who are working with you whenever you push to the branch.
    - It is possible to automate this with a slack bot - we can look into this if it becomes an issue.
- HTML doesn't need to use buttons for interactable elements.
- If small groups are working on a single task or set of tasks, they should be meeting independently of the larger group.
- Since we're working with web components, it might be good to split everything into templates.
- If anyone needs help, ping Ryan or Nick.

## TODOs:

-  [ ] The CRUD Functions
-  [ ] The Unit Tests for the CRUD functions
-  [ ] Integration Testing
-  [ ] Code Coverage Testing
-  [ ] Code Quality Checking
-  [ ] Standards for Compatibility Testing
-  [ ] Visual Aspect - CSS and Rendering

## Summary

During this meeting, we had a sprint review and discussed certain particular design choices that still needed to be made / modified.

- The primary repository is the Flash Card repository.
- The CRUD functions are on the way and should be done by this sprint.
- The recording feature will only contain a single recording, rather than ten.
- The CI/CD pipeline - in its current iteration - has been clearly outlined.
- There is a lot of work to be done with regards to testing.