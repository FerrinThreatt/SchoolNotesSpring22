# CPSC 2150 Notes 1/19/2022

## Core Concepts

### Encapsulation
-Grouping related data operations together
-We do this with classes and objects
   -State
   -Methods
-Doing this allows us to keep our data in sync

---

### Information Hiding
-Information Hiding and Encapsulation are often confused as the same thing, but they are different
-Information Hiding is how we control access to encapsulated data and operations. (Basically we don't want people knowing our code)
    -Done by using visibility settings
		- `public`
		- `private`
		- `package private`
		- `protected`

### Why Hide Information?
- To keep data in sync
- To keep accurate data
- To keep data secure
- To not overwhelm other programmers with implementation details.
    - This means that the person programming code, doesn't have to know everything about the code, just the basics

---

### Seperation of Concerns aka Modular Design 
- Each module has its own specific role
- Work together to solve more complex problems
- Objects and Classes are Modules

> A good design helps with re-useability, debugging, and adapting to change

---
