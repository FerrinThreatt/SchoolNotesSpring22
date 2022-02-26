# CPSC 2150 Notes 1/24/2022

## Design by Contract

### Contrracts
- Helps define responsbilties
- Formal or Informal

---

### Precondition
- Defines the clients responsibilities
- Defines what is true BEFORE calling the code
    - Steps that need to have already happened
    - Can be related to the parameters
    - Can be  the current state of the object   
- Need to ask the question:
    - What would cause this code to fail
- Not everything will have a precondition

### Postcondition
- Defines the Implementers responsibilties
- Defines what is true AFTER calling the code
- Tells the client what the code does
    - Return value
		- Events
		- Sate of the object
- Allows us to know information about our variables

---

### Separation of Concerns
- Gives responsibilities to each role
- Tells you what you can assume
- Implementer
		- Assumes precondition is true
		- Responsible for post condition
- Client
		- Responsible for pre condition
		- Assumes postconditions will be true

---

### JavaDocs
- Comments in Code that define a contract

---

### Contracts Use
- #var
	  - The original value stores in var
			   - AKA number does not change
- Am I meeting the precondition
		- Does it evaluate to true
- What will happen to the code
		○ Post condition
- Am I meeting the postcondition

---

> Preconditions and Postconditions were about things that are True before and after some method call or event


### Example 1
	`public class Exercise1 {`
	/**
	 * Determine the number of days in month {@code m} of year {@code y}.
	 * <p>
	 * <b>NOTE:</b> April, June, September and Nov have 30 days.
	 *
	 * @param m: representing the month
	  * @param y: representing the year
	 * 
	 * @return 
	 * 
	 * @pre:
	  *   m >= 1 AND m <= 12 
	  *    y > 0
	 * 
	 * @post:   
	 *  daysInAMonth = 31 iff (m in [1,3,5,7,8,10,12])
	 *  daysInAMonth = 30 iff (m in [4,6,9,11])
	 *  daysInAMonth = 28 iff (m=2 AND !isALeapYear)
	 *    daysInAMonth = 29 iff (m=2 AND isALeapYear)
	 */
	`public int daysInAMonth(int m, int y) {}`

---

	/**
	 * Determine if the year {@code y} is a leap year.
	 * <p>
	 * <b>NOTE:</b> {@code y} is a leap year if, divisible by 4, 
	 * but not divisible by 100 unless also divisible by 400, 
	 * then it is a leap year.
	 *
	 * @param y
	 *
	 * @return 
	 *
	 * @pre
	 * isALeapYear = true iff (y%4=0 AND y % 100 !=0 OR y%400=0)
	 * 
	 * @post
	 * 
	 * 
	 */
	`public boolean isLeapYear(int y) {}`

---
