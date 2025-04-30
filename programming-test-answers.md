# Programming Test Answers

## Exercise 1: Task 1
- **Question**: Write a program in the language of your choice where:
  - The iteration number (starting from 1), followed by a random number between 1 and 100, is printed 100 times.
  - After every 5 iterations, write an additional separator (e.g., `---`).
  - Write “Lucky number!” after every random number that is divisible by 7.
  
- **Answer**:
  ```Javascript```
  # My solution here
  
   /* Thanks to the question structure, it helped me break the problem down into smaller sub problems,
       which made it easier to approach and solve each parts step by step :) 
    */

  for ( let i = 1; i <= 100; i++ ) {    //step 1 loop from 1 to 100
  // step 2 Used Math.floor with Math.random to generating numbers from 1 to 100 and stored the result in variable
    const randomNumber = Math.floor(Math.random() *100) +1;   
    console.log(`Number: ${i} -> ${randomNumber}`);
  
    if ( i %5 === 0) {   // After every 5 iteration it will print ---
        console.log("---");
    }
    if ( randomNumber %7 === 0) {   // If randomNumber is divisible by 7 it will print Lucky Number
        console.log("Luccky Number");
    }
  }

  // 🤔 My Approach & Learnings
  /*This question helped me brake down a problem into smaller part even though it was already in points but it made things more clean and understanding
  and help in solving each part logically.
  Using Javascript Math.floor and Math.random to control the number range.
  The last part was very interseting to print "Lucky Number" if the random number is divisible by 7. 
  */



   ## Exercise 2

### 1. **What is your understanding of the term “Design Patterns”?**  
   Provide a description in your own words.

### 2. **Explain the MVC Pattern**  
   - What does MVC stand for?  
   - Explain the pattern in detail.  
   - What are some use cases for this framework?

### 3. **List three other design patterns**  
   - Provide names and details for three additional design patterns.
   - Explain how you have used those patterns in the past and how they have solved your problem  
   - Use diagrams to explain the design patterns.

- **Answer**:

   - #1 
    Design patterns are reusable solution for common problems. This provide a clear and structual way of code for making things more reausable flexible and easy to maintain which helps developer write code much more clear and efficient.

   - #2
   - MVC stand for Model View Controller.
   - // Correction: This part was originally written here by mistake.
     // It has been moved to Exercise 3 - Question 2 where it belongs.

   - #3
   -
   - In the past i created a project (Movie database) using react.js i used a structure similar to MVC without formally implementing it.
     Model 🧠 -> I used state to manage the movie database Favourite movies and API responses
     View 👁️ -> What the users saw - react components render the ui- movie cards, search bar, layout and banners.
     Controller 🎮 -> The functions which handles all the clicks or search movie and update data.

     /* At starting i wasn't familiar with the MVC pattern before this exercise. But after doing some research and understanding, i realized thati had already used a similar structure in my past projecct which was react based movie database project. Understanding the concept of MVC helped me see naturally seperated data (Model) UI (View) and Logic (Controller) even if I was not knowing the patter name at the time.
     */ 
   - Diagram image -> Exercise-2-mvc-diagram.jpg 


   ## Exercise 3

### 1. **Implementation Task**  
   Based on the class diagram below, provide an implementation in any object-oriented programming language of your choice.
   
```mermaid
classDiagram

class A {
	# Name : string
	+ PrintName() void
}

<<abstract>> A

class B {
	- PrintName(message : string) void
}

class C {
	+ PrintName(message : string) void
}

D --|> A
B --|> A
C --|> B
```

### 2. **Key Questions**  
   - Are you able to directly create a new instance of `ObjectA`? Please explain your answer.  
   - Given an instance of `ObjectC`, are you able to call the method `PrintMessage` defined in `ObjectB`? Please explain your answer.  
   - Try to explain as many key features of object-oriented programming as you can find in this example.

- **Answer**:
// the class A with name and funciton to print it
//As from the question I know that class A is an abstract so you cant use it directly.
class A {
    constructor(name) {
        this.name = name; // saves the name
    }

    PrintName() {
        console.log("name is:" this.name);  //print the name
    }
}

// class D gets everything from class A
class D extends A {}

// a new D and give it a name
let d = new D("Yangbel");

// Call the function to print the name
d.PrintName(); // Output: Name is: Yangbel


/* I come from a strong web development background, so I haven’t used abstract classes or private methods in JavaScript before. But I understand this diagram is about inheritance and method visibility. I tried to follow the structure logically and write what I could. I'm eager to learn these deeper OOP concepts more seriously now. */

- 2
- #1 No, I cannot directly create an instance of ObjectA in JavaScript because abstract classes are typically used as blueprints for other classes to inherit from. Though in JavaScript, we don’t have a true abstract keyword, I understand that abstract classes are designed to provide a structure and cannot be instantiated directly. This idea is like using a parent class as a foundation for other classes, which is what I've done with class D inheriting from class A.

Since A has a constructor, we can inherit it, but we need to create a subclass (like D) to actually instantiate and work with objects. I’ve tried following this idea by using inheritance, and though I haven't fully explored abstract classes or private methods in JavaScript before, I plan to learn these concepts more deeply.

- #2 I wasn't able to implement ObjectC or ObjectB because i am still learning about inheritance and access control like private and public key in javascript.
  What i understand from this was: ObjectC inherits from ObjectB and if the method PrintMessage in ObjectB is not private then ObjectC should be able to access and if its private (like #PrintMessage) then it is not accessable from ObjectC.

- #3 I am still understanding nad learning the concept and going deep in it but what i have understand while working on this:
  Inheritance: I understand that how one class can get properties and method from other. eg(I usedd class D extends  A which means D is inherit from A).

  Abstraction: I found out that its more like a blueprint and you can't directly create an object from the class. eg (if we try let a  = new A("Test)this is not allowed) like orther OOP languages like Java or c++ it will direct show error. As i found out javascript doesn't have a build in abstract classes so may we can do something like eg-> if(new.target === A) throw new error ("cannot directly abstract class A") the new.target will check if if you are trying to create A directly if you do it will print error.

  Encapsulation: I noticed that properties like name can be kept protected or privatae. eg-> ( constructor(name) so its a function works when you create a new object from class and the (name) is the parameter) but also now i understand real private ones use # in javascript.

  Polymorphism: I didn't use this fully, but i understand that you can define the same method in different ways in different classes like eg-> (PrintName() can be redefined in child class where one class can have different output like "Hello" and other as "hello yangbel" even if we used the same PrintName()).

// I'm still learning advanced OOP concepts.
//I focused on what I understood: inheritance, constructor, and method calling.
//I will imporve my knowledge of abstraction and polymorphism with more practuce and implement in real world projects.