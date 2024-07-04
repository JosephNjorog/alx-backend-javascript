# 0x04. TypeScript Project

## Overview
This project demonstrates my understanding of TypeScript by creating and working with interfaces, classes, functions, and namespaces. The project includes tasks such as defining interfaces, extending classes, creating functions, and using namespaces. Each task showcases different features and capabilities of TypeScript.

## Learning Objectives
By the end of this project, I was able to explain:
- Basic types in TypeScript
- Interfaces, Classes, and Functions
- Working with the DOM and TypeScript
- Generic Types
- Using Namespaces
- Merging Declarations
- Using Ambient Namespaces to import an external library
- Basic Nominal Typing with TypeScript

## Tasks

### Task 0: Creating an Interface for a Student
1. **Copy Configuration Files**
   - I copied `package.json`, `.eslintrc.js`, `tsconfig.json`, and `webpack.config.js` into the `task_0` directory.
2. **Define Student Interface**
   - In `task_0/js/main.ts`, I defined an interface named `Student` with properties `firstName`, `lastName`, `age`, and `location`.
3. **Create Students and Render a Table**
   - I created two student objects and an array `studentsList` containing these students.
   - Using Vanilla JavaScript, I rendered a table displaying each student's `firstName` and `location`.
   - I ensured that Webpack returned no type errors and all variables used TypeScript.

### Task 1: Let's Build a Teacher Interface
1. **Copy Configuration Files**
   - I copied `package.json`, `tsconfig.json`, and `webpack.config.js` into the `task_1` directory.
2. **Define Teacher Interface**
   - In `task_1/js/main.ts`, I defined an interface named `Teacher` with properties `firstName`, `lastName`, `fullTimeEmployee`, `yearsOfExperience` (optional), `location`, and allowed additional properties.
3. **Create and Log Teacher Object**
   - I created a `Teacher` object with various properties and logged it to the console.

### Task 2: Extending the Teacher Class
1. **Define Directors Interface**
   - In `task_1/js/main.ts`, I defined an interface `Directors` extending `Teacher` with an additional property `numberOfReports`.
2. **Create and Log Director Object**
   - I created a `Directors` object and logged it to the console.

### Task 3: Printing Teachers
1. **Define and Implement printTeacher Function**
   - In `task_1/js/main.ts`, I defined a function `printTeacher` that accepts `firstName` and `lastName`, and returns a formatted string.
   - I defined an interface for the function.

### Task 4: Writing a Class
1. **Define and Implement StudentClass**
   - In `task_1/js/main.ts`, I created a class `StudentClass` with a constructor accepting `firstName` and `lastName`, and methods `workOnHomework` and `displayName`.
   - I described the class and constructor through interfaces.

### Task 5: Advanced Types Part 1
1. **Define Interfaces and Classes**
   - In `task_2/js/main.ts`, I defined `DirectorInterface` and `TeacherInterface` with respective methods.
   - I implemented `Director` and `Teacher` classes based on these interfaces.
2. **Implement createEmployee Function**
   - I created a function `createEmployee` that returns a `Director` or `Teacher` instance based on the salary argument.

### Task 6: Creating Functions Specific to Employees
1. **Define and Implement Functions**
   - In `task_2/js/main.ts`, I defined `isDirector` and `executeWork` functions. `isDirector` checks if an employee is a director, and `executeWork` calls specific methods based on the employee type.

### Task 7: String Literal Types
1. **Define and Implement Subjects and teachClass Function**
   - In `task_2/js/main.ts`, I defined a string literal type `Subjects` allowing values `Math` or `History`, and a function `teachClass` that returns respective teaching messages.

### Task 8: Ambient Namespaces
1. **Setup Configuration and Define Types and Interfaces**
   - I copied configuration files into `task_3`.
   - In `task_3/js/interface.ts`, I created a type `RowID` and an interface `RowElement`.
2. **Create and Implement Ambient File**
   - I created `crud.d.ts` in `task_3/js` to declare types for `crud.js` functions.
   - In `task_3/js/main.ts`, I used the declared types and imported functions from `crud.js` to manipulate rows.

### Task 9: Namespace & Declaration Merging
1. **Setup Configuration and Define Namespaces and Classes**
   - I copied configuration files into `task_4`.
   - I created `Teacher.ts`, `Subject.ts`, `Cpp.ts`, `React.ts`, and `Java.ts` in `task_4/js/subjects` with respective interfaces, classes, and methods in the `Subjects` namespace.
2. **Merge Declarations and Implement Methods**
   - I used declaration merging to add attributes to the `Teacher` interface and implemented methods in respective classes.

### Task 10: Update main.ts
1. **Setup and Implement main.ts**
   - In `task_4/js/main.ts`, I exported constants `cpp`, `java`, and `react` for respective subjects.
   - I created a `Teacher` object `cTeacher` and logged requirements and available teachers for each subject.

### Task 11: Brand Convention & Nominal Typing
1. **Setup Configuration and Define Interfaces and Functions**
   - I copied configuration files into `task_5`.
   - In `task_5/js/main.ts`, I created interfaces `MajorCredits` and `MinorCredits` with a brand property.
   - I implemented functions `sumMajorCredits` and `sumMinorCredits` to sum credits of subjects.

## Conclusion
This project covered various aspects of TypeScript, including interfaces, classes, functions, namespaces, and advanced types. Through these tasks, I gained a deeper understanding of TypeScript's capabilities and how to effectively use it in real-world applications.
