# ADR  
**Duplicate Deck Name Handling**  
**Date: 6/5/2025**

## Context / Problem  
In our flashcard application, users can create multiple decks. Without proper checks, it is possible to enter duplicate deck names, which can lead to confusion, data management issues, and UI inconsistencies. We need a clear and user-friendly policy to handle name duplication at the deck creation stage.

## Options Considered  
- Allow duplicate names and differentiate decks by internal IDs  
- Allow duplicate names but warn users  
- Prevent duplicate names with error message  
- Automatically append a number to duplicate names (e.g., "Deck (2)")

## Decision & Outcome  
We will **prevent duplicate deck names** by validating the input at creation time. If a user attempts to enter a name that already exists, an error message will be displayed, and the deck will not be created.

## Pros & Cons  

### Pros  
- Prevents confusion between decks with identical names  
- Ensures cleaner, more organized data storage  
- Simplifies logic when accessing decks by name  
- Enhances user experience by providing clear feedback  

### Cons  
- Requires real-time validation against existing names  
- May slightly restrict user freedom in naming preferences  
