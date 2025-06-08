# ADR  
**Feature Design: User-Defined Time Target per Card vs Session Timer Only**  
**Date: 6/6/2025**

## Context / Problem  
The initial feature plan allowed users to define a time target for each flashcard during creation (e.g., “I want to review this card in 10 seconds”). However, this added unnecessary friction to the creation process, increased data complexity, and offered limited value during actual study sessions. We need a more streamlined approach to time tracking that aligns better with user goals.

## Options Considered  
- Allow user-defined time targets per card  
- Implement a single timer for the overall study session  

## Decision & Outcome  
We will **remove the per-card time target input during card creation** and instead **implement a session-level timer** to track total study duration.

## Pros & Cons  

### User-Defined Time Target per Card  

#### Pros  
- Custom pacing goal per card  
- Could inform personalized feedback or analytics  

#### Cons  
- Increases friction during card creation  
- Adds unnecessary complexity to card data schema  
- Minimal benefit compared to effort and UI clutter  

### Session Timer Only  

#### Pros  
- Cleaner, simpler user experience  
- Easier to track study consistency and total time spent  
- Better alignment with standard spaced repetition practices  

#### Cons  
- No individualized pacing data  
- Cannot identify unusually slow or fast cards
