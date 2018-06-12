# Meaningful Names

### Use intention revealing names

- `int d; // elapsed time` is bad
- `int elapsedTimeInDays;` is much better

### Avoid disinformation

- Don't call something an `accountList` if it's not a list
- Avoid long names that are very similar and hard to distinguish
- Names for similar things should group together for autocomplete

### Make meaningful distinctions

- Do not append something to a variable because the name you wanted was already taken in the scope
- Do not add numbers on to variables e.g. `a1` a2` `a3` 
- Avoid adding noise like `ProductInfo` or `ProductData`
- Avoid redundancy, do not put variable in a variable name or do things like `NameString` or `CustomerObject`

### Use pronouncable names
- They're easier for humans to talk about and rememebr

### Use searchable names
- Searching across a codebase for something like the number 7 is very hard. Assign it to a constant

### Avoid mental mapping

- Don't make the reader try to remember what a variable name like `r` means, call it what it means

### Class names

- Class names should be nouns, not verbs
- Avoid names like Manager, Processor etc. 

### Method names

- Use verbs
- For overloaded constructors, gove them a name that describes their arguments = `fromRealNumber()`

### Don't try to be funny

- Don't use memes or jokes in your names

### Pick one word per concept

- Don't use `fetch`, `get` and `retrieve` all at once
- Don't have a `Manager` and a `Controller`

### Don't say one thing when you mean something else

- If you have a bunch of classes with an `add` method which behaves in a certain way, don't add a new class and method which do something different

### Use solution domain names

- Your audience are programmers, so it's ok to use CS and programming concepts to name things e.g quque, visitor

### Use problem domain names

- When there's no equivalent CS concept for what you're tryig to do, use a name from the problem domain. The programmer can always look it up if they need to.

### Add meaningful context

- Try to place your variables within a class or namespace which adds context for the reader
- If this is not possible, adding a prefix might be a good idea

### Do not add gratuitous context

- If your app is DeluxeGasStation you should not prefix everything with GDS e.g. `GDSCustomer`

