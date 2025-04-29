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