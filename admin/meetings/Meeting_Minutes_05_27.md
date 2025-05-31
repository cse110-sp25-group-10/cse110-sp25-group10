# Team 10x - May 27 Meeting Minutes

## Table of Contents

- [Team 10x - May 27 Meeting Minutes](#team-10x---may-27-meeting-minutes)
  - [Table of Contents](#table-of-contents)
  - [Attendance](#attendance)
  - [Meeting Agenda](#meeting-agenda)
  - [Talking Points](#talking-points)
    - [Javascript](#javascript)
    - [Testing](#testing)
    - [CSS](#css)
    - [Retrospective:](#retrospective)
  - [Questions](#questions)
      - [Question: What should the Delete Card function do?](#question-what-should-the-delete-card-function-do)
  - [TODOs](#todos)
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

1. Sprint Review
2. TODOs

## Talking Points

### Javascript

The people working on the Javascript functionality did **very** well this sprint.

- The primary goal for this sprint was to complete the CRUD functions. These are effectively done.
- The Rendering functionality has some slight things that must be ironed out.
- We also considered event delegation. No direct verdict on this was given.

The main important thing that must be worked on now is validation checks.

- Currently, we have alert dialogs in place.
- There are other simple ways to give feedback to the user when things go wrong. (Making the border go red, etc.)

The next thing on the board for the Javascript team is the **Practice Study Screen**.

### Testing

The following tests have been written:

- Create Card
- Delete Card
- Create a Deck
- Other CRUD functions except SHUFFLE
- Taha worked on additional tests for his own code.

To prepare for the following sprint, we want to have some sort of end-to-end testing done to make sure users can move around the screens properly.

*Note: We want to do this manually for now - automation will not work, as the UI is still being built in CSS.*

### CSS

The home page has been completed, though the buttons still need to be done.

There are several other screens that must be implemented.

The CSS and HTML teams are heretofore merged, in order to more evenly distribute the workload and get things done on time.

### Retrospective:

1. We had a lot of merge conflicts - at least three were seen just the morning of this meeting.

    - Remember, when working on a branch with others, ensure active communication is taking place. 
    - Try pair coding through VS Code Live Share if possible.
2. We have had some communication issues throughout this sprint.
3. We are still behind.
4. There is some old code in the repository that is confusing, and should probably be cleaned up.

## Questions

#### Question: What should the Delete Card function do?

**Answer:** The delete card function should remove the card from the deck, and return the card that was removed.

Think of the notion of "popping" an element from a data structure.

Currently, it just returns a single card. When it is not successful / does not delete a card, it should return null.

We should incorporate some checks as well to make sure that the card returned was correct, we actually deleted the card from the deck, and that the deck size is smaller.

## TODOs

- [ ] Finish all base CSS
- [ ] Finish Unit Testing for all JS functions
- [ ] Finish form validation.
- [ ] Practice Section
  - [ ] Timer System
  - [ ] Cycling between cards using Next, Previous buttons.
  - [ ] Add Recording functionality
- [ ] Clean Up Rendering

In short: The app should be **fully functional** this week - by Sunday at the latest!

## Summary

1. The Javascript team did well and accomplished the primary goals for this sprint!
2. We want to incorporate end to end testing in addition to the unit testing suite developed during this sprint.
3. The CSS team has been enlarged to include all who worked with HTML.
4. The app should be *effectively* complete by Sunday.