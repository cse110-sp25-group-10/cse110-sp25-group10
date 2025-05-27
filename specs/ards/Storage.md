# ADR  
**Local storage implementation**  
**Date: 5/26/2025**

## Context / Problem  
The application needs client-side storage to persist user data, such as flashcard progress, custom decks, and potentially offline access to content. The chosen storage solution must support structured data, scalability, and performance for read/write operations.

## Options Considered  
- **LocalStorage**: Simple key-value storage available in all browsers  
- **IndexedDB**: Asynchronous, object store-based, client-side database with structured querying  

## Decision & Outcome  
We will use **IndexedDB** for client-side storage. Its capabilities are better suited for handling complex and larger-scale data operations required by our app. Needed for the audio feature we are planning to implement.

## Pros & Cons  

### Pros (IndexedDB)  
- Supports complex data types (objects, arrays)  
- Asynchronous and non-blocking, avoiding UI freezes  
- Stores significantly more data than LocalStorage (hundreds of MBs vs ~5MB)  
- Can index data for faster queries  
- Allows transactions and cursor-based iteration for large datasets  

### Cons (IndexedDB)  
- More complex API than LocalStorage  
- Requires handling versioning and upgrade logic  
- Harder to debug manually (though browser DevTools support it)  

### Pros (LocalStorage)  
- Very simple API (`setItem`, `getItem`)  
- Easy for quick prototyping  

### Cons (LocalStorage)  
- Only stores strings (requires serialization)  
- Very limited storage space (~5MB)  
- No indexing or query support  

## Conclusion  
While LocalStorage is easy to use, it does not meet the data complexity or scalability needs of our application. **IndexedDB** provides the necessary structure, performance, and flexibility for a robust client-side data layer.
