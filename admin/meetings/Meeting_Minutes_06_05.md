# Team 10x - June 05 Meeting Minutes

## Table of Contents

- [Team 10x - June 05 Meeting Minutes](#team-10x---june-05-meeting-minutes)
  - [Table of Contents](#table-of-contents)
  - [Attendance](#attendance)
  - [Meeting Agenda](#meeting-agenda)
  - [Talking Points](#talking-points)
    - [Current Priorities](#current-priorities)
    - [Testing](#testing)
    - [Polish / Quality of Life Changes](#polish--quality-of-life-changes)
  - [Questions](#questions)
    - [Card Navigation in the Create a Deck Screen](#card-navigation-in-the-create-a-deck-screen)
    - [Deployment](#deployment)
  - [Professor Powell's Feedback](#professor-powells-feedback)
    - [First Impressions](#first-impressions)
      - [The Identity Test](#the-identity-test)
      - [The "Create" Button](#the-create-button)
      - [The "Study, Edit, Delete" Panel](#the-study-edit-delete-panel)
    - [Resizing](#resizing)
    - [The "Create Deck" Screen](#the-create-deck-screen)
      - [Anticipating User Flow](#anticipating-user-flow)
      - [Closure](#closure)
    - [Key Takeaways:](#key-takeaways)
  - [Post-Feedback Discussion](#post-feedback-discussion)
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

1. Final Sprint Planning

## Talking Points

### Current Priorities

Currently, the biggest thing that we  need to get done is the practice screen. The basic HTML mockup is ready to be split up. The Javascript must be done as soon as possible. 

Notes for the Javascript team: Don't focus too much on rendering until the **actual functionality** is there - this means shuffling the deck, swapping, the timer, etc.

*Note: When implementing the timer, we want the timer to count **up** during Practice mode, and **down** during presentation mode.*

### Testing

We are also currently in polish mode - here are some things to keep in mind for the rest of the sprint.

1. We must test on several devices.
2. Keep figuring out novel ways to interact with the app in order to ensure maximal stability, accessibility, and robustness.

If we find any issues when exploring in the above way, please notify the rest of the team through Slack.

Here are some additional points brought up during the meeting:
1. Make sure we have looked at the pipeline - there is a diagram in the "admin" section of the home repo, in which any names correspond to files to be found in the flashcard repo.
2. There is a known issue with low code coverage - much of our code simply cannot be reached without end to end testing.
3. We will be using "Puppeteer" as the frameowrk for end to end testing.

### Polish / Quality of Life Changes

Ryan came up with a few things that can be changed in order to improve the Deck Creation screen:

- Remove the "Save a Name" requirement before you can add cards.*
- You need counters to let you know how many characters you can type as you input the card data.
- You need a hover tooltip with the timer logo, to better communicate to the user what is going on with that input.
- Remove the arrows on the sides of the deck creation screen - [these will unfortunately probably not be implemented.](#card-navigation-in-the-create-a-deck-screen)

Here were some suggestions that were brought up for further quality of life changes:

1. Someone mentioned that we should be able to save an unnamed deck.
   - The argument **for** this is that it is a **natural thing to do** when working in most other applications - think "Untitled Document" in Google Docs.
   - The argument **against** this is that it is simply too late to change this at this stage - not to mention that *the naming system is bugged (A deck with the same name as an existing deck overwrrites the old one)* and the current fix for that is incompatible with this sugggestion.
   - Our **final verdict** is that we will **not** implement the requested change. the Iron Triangle dictates that we must balance between our limited temporal resources and what we need to have in the project at the time of release.
2. We need an easier way to access the URL - someone suggested to put it in the ReadMe.

## Questions

### Card Navigation in the Create a Deck Screen

We have two options for navigating between flash cards up and down. Unfortunately, we don't have this implemented. Do we continue with this feature?

- One option is to leave this as a **TODO** feature - recalling that we are "handing off" the project to Rashi for "further development." 
- The other option is to try rushing this - but it might be a mistake to invest our limited time here.

Our **final verdict** is to **leave this feature as a TODO feature.** The Card Study screen still has yet to be implemented, and that is significantly more important. 

It is possible that we will keep the buttons and tell the user that they will be functional in a "later update" or "upcoming feature." This is to be determined.

### Deployment

Throughout the project, Rashi has told us that deploying on GitHub Pages will give us issues. However, we don't have much of a deployment strategy outside of this, nor are we sure why we were given these warnings.

Professor Powell gave the following information:

- If we were to consider in terms of professional production quality, Rashi is correct to say that GitHub Pages is not the right call.
- We must consider that all deployment platforms will have tradeoffs - using GitHub Pages is built into GitHub, but if we can pull it off, the app will be more performant and professional.
- Netlify and Cloudflare are free alternatives - Firebase is another possible alternative, but it is the hardest.
  - Netlify and Cloudflare are also very easy and reliable for apps that do not use the network, like ours.
  - We also have members (Ryan and Nick) who have experience using Netlify.
- We got the warnings that GitHub Pages wouldn't work because **on GitHub Issues, there is no possibility for authentication or logs**.
- In practice, GitHub Pages is only really used for docs and wikis.

With all of this considered, we have decided to use **Netlify** to deploy our application.


## Professor Powell's Feedback

### First Impressions

#### The Identity Test

Upon opening the app, Professor Powell immediately noted that our application **fails the identity test**.

- On first glance, it should be clear what the user is meant to be looking at.
- The header talks about a study app, but the planets in the background imply other possibilities.

(It should be noted - Professor Powell examined the app for a good deal of time, and gave absolutely no indication that he understood this to be a **speech preparation app** rather than an academic study app)

#### The "Create" Button

The Create Button should probably be in the center of the screen - the big blue block in the center is the big "attention grabber" on this screen.

The button should also be clearer in its purpose - one possible option is to have it say "Create **study deck**, for instance.

#### The "Study, Edit, Delete" Panel

There were mixed reviews of the "Study, Edit, Delete" panel at the bottom of the screen.

On the one hand, it might be nice to have so that it's not a surprise when a deck is selected.

On the other hand, it could be argued that it is a distraction at this stage, since you can't do anything with it yet.

### Resizing

Resizing works, which is a very good sign. Many teams do not even have this.

### The "Create Deck" Screen

#### Anticipating User Flow

Upon opening the screen, Professor Powell found himself asking, "What am I supposed to do here?"

English readers begin reading from top left, so when scanning the screen, the **first thing you do** should be there. In our app, we have the less appropriate "Save and Finish" button there.

The user is intended to create a speech name, then the front of a card, then the back of a card... there's a lot to do here!

One suggestion is to do everything **one at a time** so that the user doesn't have to worry about going forwards and backwards.

(There are obvious pros and cons to this solution.)

Here's a potential implementation guide for "Step Sequencing."

1. Give elements a data attribute data-step.
2. Keep the current step tracked, and increment as the user works through each one.
3. Show the elements whose data-step attribute matches the current step.

With just a couple lines of javascript, we can turn what we have into a simple "wizard" or "sequencing" style input form.

A final thing to note here is that the timer input field is large, which gives no indication that there will be such a small range of inputs (1-60) - it might be worth reducing the size of this field.

This screen should also be **tabbable** - tab indexing and autofocus attributes are small but vastly improve polish.

The trick is to play **UI GOLF** - the least amount of movement to perform an action wins.

To the user, it should feel like the next task appears right where they just were.

The Upload Button could also be a more intuitive icon.

(Note: The Professor seemed to think that the upload button was for file uploads. This indicates that the current name is innappropriate and confusing.)

#### Closure

After completing a task, such as making a card, there should be a sense of closure. In our app, this does not occur.

As such, the professor argued that it doesn't make sense for single edits nor bulk edits of cards.

### Key Takeaways:

1. CRUD Apps are hard. At the ennd of the day, the professor just wants to see craft and care - it's the polish that will make us stand out.
2. Make a FAKE DECK right now - using real speech content. 
   - What people see in the video is **what they think the app is** - *and you don't even need the app **working** to do that!*
   - Make it funny, real, and polished.
3. The primary issue is flow. Reduce the friction that is present in the app.
    - Think of your users as super literal, super disengaged, or impatient. Cater to these extremes to find the friction in your app.
    - At the end of the day, it's not about the precise number of steps as much as how they **feel**.
     - If the pap is polished, you'll be able to race through it!

## Post-Feedback Discussion

Based on our feedback from today, we'll likely try to split up the deck creation process.

1. Make a deck name when you create the deck, as a pop-up, rather than as part of the card creation screen.
2. When in the card creation screen, the deck name can be editable - like in Google Docs, for instance.
3. Delete the "Save and Finish" button and rename "Upload" to "Add Card" or something similar.
4. Have a "View All Cards" window. (This one is contested as many of us like the scrolling option).
5. Confirmations should be added for closure.
6. Cancel and Save should be added for when you're editing a card.

## Summary

This was the final in-person meeting of the quarter, and we had much to discuss.

1. There are public and private videos to be made. See the Canvas page for details.
2. We are not able to reorder the cards, and likely won't be able to by the end of the development cycle.
3. We will be deploying the app on netlify.
4. THe professor pointed out several issues pertaining to the "flow" of the deck creation screen. Time is limited but we should seek to address this as possible.