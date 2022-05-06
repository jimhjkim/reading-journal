# Clean Code

#노마드코더 #북클럽 #노개북 #clean_code

## Day 1

> Verify book purchase on social media!

> April 22, 2022

## Day 2

> Chapter 1. Clean Code

> April 23, 2022

### Key points

- Lays out the motivations for writing clean code and the potential repurcussions if we check in dirty code

- Insights from prominent programmers on what writing clean code means

- 10:1 reading to writing code ratio

### Things to remember

- There will always be a need to write code even thought there are many who claim that code will be generated instead of being written.

- Bad code can put companies out of business or the total cost of owning a mess can be deterimental to company growth

- Programmers have a professional responsibility to write clean code even at the expense of pushing back against tight deadlines and schedules

- Clean code is readable

- No duplication, one thing, expressiveness, tiny abstractions

- Good code can degrade over time so maintainenace also has to be a priority

### Reflection

- With the advent of many machine learning solutions, I am curious to see if the author's hypothesis on the necessity to write code will hold in the near future.

- As a professional developer, I have a responsibility to write clean code, not just to complete requirements in the shortest amount of time. Communicating these needs to non-technical stakeholders is a skill that I should start developing.

- Making it easier to read actually makes it easier to write

- Leave the campground cleaner than you found it

### Things to further investigate

- What does code that has been take care of look like?

- How does one develop code sense?

## Day 3

> Chapter 2. Meaningful Names

> April 24, 2022

### Key points

- Use intention-revealing names and be serious about it!

- Use pronounceable and searchable names

- Pick one word per concept

### Things to remember

- Choosing good names takes time but saves more than it takes

- Avoid words whose entrenched meanings vary from our intended meaning (e.g., hp, aix, sco)

- Try not to add data types/encodings to the variable names

- Beware of names which vary in small ways

- Use consistent spelling to support automatic code completion in modern development environments

- Avoid using lowercase "L" and uppercase "O" as variable names as these are easily confused with "1" and "0", respectively

- Do not make minor modifications to please the compiler

- Use pronounceable names to support intelligent conversations

- Single letter variable names should only be used as local variables to support better searching

- The length of a name should correspond to the size of its scope

- Using the same word for "consistency" across class methods can increase clarity

### Reflection

- Thinking twice about variable names can go a long way in writing clear and professional code

- Suggesting these best practices may or may not be received well by other developers but it's best to try

- Naming is partly dependent on shared culture understanding. I wonder how this is achieved in more multicultural environemnts.

### Things to further investigate

- As I write code and explore new codebases, I should look out for these naming best practices and try to implement them.

## Day 4

> Review concepts by reading 3 posts by other participants

> April 25, 2022

### Post #1 by `cho7448-3divcs`

- I liked the fact that she pointed out the "shared culutural" understanding as a key point from the chapter.

- I liked how every point from the chapter was summarized with examples listed in parenthesis.

- Reflection on how we try to put every detail into variable names is relatable.

### Post #2 by `npolly7`

- Very concise summary of the chapter

- Reflection on how including encoding in the variable name helped the writer at work made me think twice about the advice given in the chapter as well.

### Post #3 by `minn`

- Reflecting on past professional experiences where bad variable names hampered development is encouraging me to think twice before choosing variable names at work

## Day 5 - 6

> Chapter 3. Functions

> April 26 - 27, 2022

### Key points

- Functions should be small

- Avoid mixing levels of abstraction; to keep a function at one level of
  abstraction, make sure the code read like a top-down set of TO paragraphs

- Try to minimize the number of arguments passed to a function. Arguments
  impair understanding and testability. Output arguments are harder to
  understand than input arguments.

### Things to remember

- Functions are the first line of organization in any program.

- Each line should contain no more than 150 characters and each function should
  be no longer than 20 lines

- Statements such as "if", "else", and "while" should be one line long and that
  line should be a function call (keeps the enclosing function small and also
  adds documentary value with a descriptive name)

- Indent level of a function should not be greater than one or two

- Functions should do one thing. They should do it well. They should do it only.

- Check if you can extract a part of the function into another function without
  restating its implementation to see if the original function is doing one
  thing only

- Functions that do one thing cannot be reasonable divided into sections.

- Switch statements often violate many of the rules for functions. We cannot
  always avoid switch statements but we can use polymorphisms to bury them in
  a low-level class and is never repeated.

- A long descriptive name is better than a short enigmatic name.

- A long descriptive name is better than a long descriptive comment.

- Passing boolean flags as arguments is confusing and should be avoided. Create
  two functions to represent the behaviours.

- Grouping arguments in to objects and lists is not cheating as we are grouping
  concepts together.

- Have no side effects

- In general output arguments should be avoided. If your function must change
  the state of something, have it change the state of its owning object.

- Functions should either do something or answer something, but not both. Either
  your function should change the state of an object, or it should return some
  information about that object.

  - e.g., "set" -> "attributeExists" + "setAttribute"

- Exceptions are preferred over returning error codes as the latter promotes
  commands being used as expressions in the predicates of "if" statements.

- With exceptions, the error processing code can be separated from the happy
  path code and can be simplified.

- Extract the bodies of "try-catch" blocks into individual functions.

- Try to avoid duplication across the functions

- Structured programming says that every function and every block with a
  function should have one entry and one exit. If we keep our functions small,
  then we should not need to reply on structured programming.

- Do not try to write functions that follow these rules from the start. Rather,
  apply these rules during refactoring.

### Reflection

- I should try to implement these rules in my coding activities. I should also
  try to bring these points up during code review.

- Often, argument objects and lists are loaded with many values that do not
  necessarily tie together under one concept. I wonder if this is an
  anti-pattern.

### Things to further investigate

- Error codes seem to be used as much as raising exceptions. I should try to use
  more exceptions. I wonder if the disadvantages of recompiling and redeploying
  when using error codes is universal beyond Java.

## Day 7 - 8

> Chapter 4. Comments

> April 28 - 29, 2022

### Key points

- Try to rely on expressive code rather than comments

- Although there are good comments, more often than not, it is better not to use
  comments

- See if you can refactor to remove unnecesary comments

### Things to remember

- The proper use of comments is to compensate for our failure to express ourself
  in code.

- Programmers cannot realistically maintain comments.

- Truth can only be found in one placec: the code.

- Clear and expressive code with few comments is far superior to cluttered and
  complex code with lots of comments

- There are good comments!

  - Legal comments (e.g., copyright, authorship)

  - Informative comments (e.g., regular expressions)

  - Explanation of Intent

  - Clarification

  - Warning of Consequences

  - TODO Comments

  - Amplification

  - Javadocs in Public APIs

- There are bad comments!

  - Mumbling

  - Redundant Comments

  - Misleading Comments

  - Mandated Comments

  - Journal Comments

  - Noise Comments

  - Scary Noise (e.g., Javadocs)

  - Don't use a comment when you can use a function or a variable

  - Position Markers

  - Closing Brace Comments

  - Attribtuions and Bylines

  - Commented-Out Code

  - HTML Comments

  - Nonlocal Information

  - Too Much Information

  - Inobvious Connection

  - Function Headers

  - Javadocs in Nonpublic Code

### Reflection

- I love writing comments! I guess I need to think about how to express myself
  more in code effectively.

- Up until now, I thought having good communication skills as a software
  engineer was referring to engaging with different stakeholders effectively.
  This chapter is making me rethink this. Maybe communicating well with the code
  I write is what I should focus on.

- Source control systems appears to have solved a lot of inefficiences when it
  comes to comments.

### Things to further investigate

- I am curious to see how many of the comments at my work's codebase are good
  and how much of it is bad. This chapter is really helpful as it provides ample
  justification for why a comment is good or bad.

## Day 9 - 10

> Refactoring Mission

> April 30 - 31, 2021

## Day 11

> Chapter 5. Formatting

> May 1, 2022

### Key points

- Code formatting should be established as a team to communicate effectively

- Be mindful of both vertical and horizontal formatting

- Code formatting rules should be configured in each IDE and applied automatically.

### Things to remember

- Code formatting is about communication

- Style and discipline survives even though code does not

- Vertial formatting -> typically 200 lines with an upper limit of 500

- A source file should be like a newspaper article. File name should indicate whether we are in the right module or not.
  The topmost parts should provide the high-level concepts and algorithms. Details should increase as you move downward.

- Vertical Openness Between Concepts -> use blank lines to to separate different concepts (i.e., package declaration,
  imports, each of the functions)

- Vertical Density -> lines of code that are tigthly related should appear vertically dense

- Vertical Distance -> closely related concepts should be kept vertically close to each other

- Variables should be declared as close to their usage as possible

- Local variables should appear at the top of each function

- Control variables for loops should usually be declared within the loop statement

- In rare cases, a variable might be declared at the top of a block or just before a loop in a long-ish function

- Instance variables should be declared at the top of the class.

- Dependent functions should be vertically close; the caller should be above the callee

- Consider conceptual affinity when placing code vertically together

- Horizontal limit should not exceed 120

- Use white space to associate and dissociate strongly and weakly related concepts, respectively

- Prefer unaligned declarations and assignments when it comes to horizontal alignment to point out the problem of long
  list of declarations

- Breaking indentation for short if statements, while loops, or functions is not good practice

- Avoid dummy scopes (empty while or for statements) but if you cannot, indent semicolons to make clear

- Make sure each team agrees on formatting rules together and follow it going forward

### Reflection

- Often I follow code formatting conventions without thinking about why

- I do not often enjoy learning a brand new codebase but maybe I just haven't worked on a well formatted codebase

- The analogy of comparing code to a newspaper is really insightful

### Things to further investigate

- The author suggests protected variables should be avoided to keep related
  concepts vertically close. What does this mean?

- Placing the caller above the callee might not be possible in all programming
  languages...

## Day 12

> Chapter 6. Objects and Data Structures

> May 2, 2022

### Key points

- Objects expose behavior and hide data (flexibility to add new data types).

- Data structures expose data and have no significant behavior (flexibility to add new behaviors).

- Avoid creating hybrids with objects and data structures

### Things to remember

- The reason developers keep variables private is to keep freedom to change their type or implementation on a whim or an
  impulse

- We do not want to expose the details of our data. We want to express our data in abstract terms.

- Objects and data structures are different.

- Objects hide their data behind abstractions and expose functions that operate on that data.

- Data structure expose their data and have no meaningful functions.

- Procedural code (code using data structures) makes it easy to add new functions without changing the existing data
  structures. This makes it hard to add new data structures because all the functions must change.

- Object Oriented code (code using objects, duh!) makes it easy to add new classes without changing existing functions.
  This makes it hard to add new functions because all the classes must change.

- The idea that everything is an object is a myth. Sometimes you really do want simple data structures with procedures
  operating on them.

- Law of Demeter

  - A module should not know about the innards of the objects it manipulates

  - A method should not invoke methods on objects that are returned by any of the allowed functions

- Avoid creating hybrids that are half object and half data structure.

- Data Transfer Object (DTO) -> a class with public variables and no functions; sometimes getters and setters exist to
  satisfy OO purists

- Active Records are special forms of DTOs. They are data structure with public variables but also have navigational
  methods like `save`and `find`. Active Records are typically are direct transaltions from database tables or other data
  sources.

- Avoid placing business rule methods in Active Records as this creates a hybrid between a data structure and an object.

### Reflection

- I have not thought too much about the difference between objects and data structures. In fact, I treated objects as
  another data structure.

### Things to further investigate

- In JavaScript, we hear that everything is an object. I wonder if this is why some developers dislike the language as
  there are hybrids between objects and data structures everywhere!

## Day 13

> Review Quiz

> May 3, 2022

## Day 14 - 15

> Chapter 7. Error Handling

> May 4, 2022

### Key points

- Following some key rules during error handling will improve the robustness of your code

- Extracting the error handling logic from the main algorithm can be a fine balancing act

- Clean code is readable, but it must also be robust

### Thinggs to remember

- Error handling that obscures logic is wrong

- Use exceptions rather than error codes

  - Aesthetically pleasing

  - Separates concerns -> main algorithm + error handling

- Write your `try-catch-finally`statement first

- Use unchecked exceptions

- Provide comtext with exceptions

- Define exception classes in terms of a caller's needs

- Define the normal flow

- Don't return null

- Don't pass null

### Reflection

- I will need more practice with applying these rules before I fully understand them.

### Things to further investigate

- Try to apply these rules at work and ask questions
