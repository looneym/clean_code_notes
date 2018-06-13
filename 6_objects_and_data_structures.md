# Objects and Data Structures

We hide our private variables from the world so that we are free to change their types or implementation however we choose. 

### Data Abstraction 

- Interfaces enforce an access pattern which can protect our private variables and enforce data integrity
- Hiding implementation is not about adding a layer of functions, it's about abstraction. Our goal should be to expose an interface that
exposes the _essence_ of the data to users without requiring them to care about it's implementation

### Data/Object Anti-Symmetry

- *Objects* hide their data behind abstractions and expose functions that operate on that data. 
- *Data Structures* expose their data and have no meaningful functions
- These are opposites!
- Procedural code which operates on data structures makes it easy to add new functions without changing the existing data structure. If you _do_ need to 
add more data structures, all of the functions must change
- OO code makes it easy to add new classes without changing the existing functions. Adding new functions requires modifying existing classes. 
- In some systems we will want the flexibility to add new data types, in others we will want to add new behaviours. We should recognize how the system is likely to 
grow and choose the best approach
- Avoid creating hybrids of Data Structures and Objects, they are the worst of both worlds

### The Law of Demeter

- A method on a class should only call methods on it's class or variables of that class, variables passed as argments to the function, or objects it creates itself. 
- Chaining methods together across multiple classes is bad
- You should tell a class what you want it to do, not query it about it's internals (and their internals... and their internals) 

### Types of Data Structure

- Data Transfer Objects are classes with public variables and no meaningful functions. They are commonly used in the first stage of a translation pipeline 
between raw data in a database and application ojects. 
- Active Records are similar, but may contain some additional methods like `save`, `find` etc. They should not contain any additional business logic. Instead,
create otger casses for this logic which operate on Active Records. 

