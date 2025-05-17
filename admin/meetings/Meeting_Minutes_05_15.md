# Team 10x - May 15 Meeting Minutes

## Table of Contents

- [Team 10x - May 15 Meeting Minutes](#team-10x---may-15-meeting-minutes)
  - [Table of Contents](#table-of-contents)
  - [Attendance](#attendance)
  - [Meeting Agenda](#meeting-agenda)
  - [Talking Points](#talking-points)
    - [Check-in](#check-in)
    - [Features We Want To Work On And Finish By End Of Sprint](#features-we-want-to-work-on-and-finish-by-end-of-sprint)
    - [Repo Structure](#repo-structure)
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

1. State of Affairs
2. Features we want to work and finish by end of sprint
3. Addressing feedback for our repository strcuture

## Talking Points

### Check-in

- Eric Wang and Alan Shapow: 
  - Demoed basic flashcard 
- Audrey Fernandez and Loreen Samaan:
  - Showed sketch of UI
- Ryan Kung:
  - Added guidelines for HTML, CSS, and JS
- Alex Pan and Nicholas Nurwinata:
  - Basic pipline stuff with ESLint and human code review and answered questions anyone had about it
- Fong Lin and Taha Qamar:
  - Made JS for basic card creation logics and flipping
- Johnson Chung and Branden Sioson:
  - Waiting to be able to test

### Features We Want To Work On And Finish By End Of Sprint
We wanted the basic functionality to work on desktop by the end of the sprint. 
- [x] Creating flashcard
      - Set a length for each card
- [x] Being able to see flashcard
- [x] Being able to update flashcard
- [x] Being able to delete flashcard
- [ ] Voice recording
  - Pressing record shows time
  - Will probably implement last
- [x] Decks
  - For now, just want to show all cards in deck
- [ ] Study and review feature (Quizing)
- [ ] Timer on how long to say each card
- [ ] Compatibility with mobile phones
  - Low priority until it works on desktop

### Repo Structure
After some discussing, we decided to seperate our directory by components. We also decided to have a prototype folder to seperate out features we are testing.  
However, we still need to address the repos themselves. We currently have two seperate repos: one for the Flashcard Project, and the other for the Team.  
We need to combine these together.  
Someone we suggested to use Github submodules, but we are unsure if we are allowed.
#### Question We Need to Ask
Can we use a Github submodule from the Team Repo to the Flashcard Project repo?
  
## TODOs

- [ ] HTML / CSS of cards must be prototyped.
  - See: [#13](https://github.com/cse110-sp25-group-10/Flashcard-Project/issues/13)
- [ ] Javascript should be written to take user input and create components from them. 
  - See: [#14](https://github.com/cse110-sp25-group-10/Flashcard-Project/issues/14)
- [ ] Mobile and Rescaled Layouts should eventually be made. 
  - This is currently **low priority**.
  - See: [#16](https://github.com/cse110-sp25-group-10/Flashcard-Project/issues/16)
- [ ] Hard feature specifications **must** be ironed out.
  - See: [#15](https://github.com/cse110-sp25-group-10/Flashcard-Project/issues/15)
- [ ] Card Customization must be clearly defined.
- [ ] Voice recording feature
  - See: [#18](https://github.com/cse110-sp25-group-10/Flashcard-Project/issues/18)
  - Currently not working on for sprint
- [ ] Quiz feature 
  - See: [#19](https://github.com/cse110-sp25-group-10/Flashcard-Project/issues/19)
  - Currently not working on for sprint


## Summary
In the beginning of the meeting, we had a check-in for everyone's progress on their tasks.

Next, we discussed features we wanted to add and which ones we should work on and finish by the end of the sprint. We picked out the basic features for the basic functionality to work.

We also addressed the feedback about the repo structure. We decided to seperate the folders by component and add a prototype folder.
