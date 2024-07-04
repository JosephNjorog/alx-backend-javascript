# 0x03. ES6 Data Manipulation - Project README

## Overview

This project focuses on manipulating data structures using ES6 features in JavaScript. The tasks include working with arrays, typed arrays, sets, maps, and weak maps. Each task builds on the previous one to create functions that perform specific operations.

## Prerequisites

- **Node.js** (version 12.11.x)
- **npm** (version 6.11.3)
- **Jest**, **Babel**, and **ESLint**

## Setup

### Install Node.js and npm

First, I installed Node.js and npm:

```bash
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```

I verified the installation with the following commands:

```bash
nodejs -v
# v12.11.1

npm -v
# 6.11.3
```

### Install Jest, Babel, and ESLint

In my project directory, I used the supplied `package.json` file and ran `npm install` to install Jest, Babel, and ESLint.

## Configuration Files

I added the following configuration files to my project directory:

- `package.json`
- `babel.config.js`
- `.eslintrc.js`

I ran `npm install` to install the dependencies.

## Tasks

### Task 0: Basic List of Objects

I created a function named `getListStudents` that returns an array of objects. Each object has three attributes: `id` (Number), `firstName` (String), and `location` (String). The array contains the following students for example given:


- Guillaume, id: 1, in San Francisco
- James, id: 2, in Columbia
- Serena, id: 5, in San Francisco

```javascript
// 0-get_list_students.js

export default function getListStudents() {
  return [
    { id: 1, firstName: 'Guillaume', location: 'San Francisco' },
    { id: 2, firstName: 'James', location: 'Columbia' },
    { id: 5, firstName: 'Serena', location: 'San Francisco' },
  ];
}
```

### Task 1: More Mapping

I created a function `getListStudentIds` that returns an array of ids from a list of objects. If the argument is not an array, the function returns an empty array. I used the `map` function on the array.

```javascript
// 1-get_list_student_ids.js

export default function getListStudentIds(list) {
  if (!Array.isArray(list)) return [];
  return list.map((student) => student.id);
}
```

### Task 2: Filter

I created a function `getStudentsByLocation` that returns an array of objects who are located in a specific city. I used the `filter` function on the array.

```javascript
// 2-get_students_by_loc.js

export default function getStudentsByLocation(list, city) {
  return list.filter((student) => student.location === city);
}
```

### Task 3: Reduce

I created a function `getStudentIdsSum` that returns the sum of all the student ids. I used the `reduce` function on the array.

```javascript
// 3-get_ids_sum.js

export default function getStudentIdsSum(list) {
  return list.reduce((sum, student) => sum + student.id, 0);
}
```

### Task 4: Combine

I created a function `updateStudentGradeByCity` that returns an array of students for a specific city with their new grade. If a student doesn’t have a grade in `newGrades`, the final grade is `N/A`. I used `filter` and `map` combined.

```javascript
// 4-update_grade_by_city.js

export default function updateStudentGradeByCity(list, city, newGrades) {
  return list
    .filter((student) => student.location === city)
    .map((student) => {
      const gradeObj = newGrades.find((grade) => grade.studentId === student.id);
      return { ...student, grade: gradeObj ? gradeObj.grade : 'N/A' };
    });
}
```

### Task 5: Typed Arrays

I created a function `createInt8TypedArray` that returns a new `ArrayBuffer` with an `Int8` value at a specific position. If adding the value is not possible, the error `Position outside range` is thrown.

```javascript
// 5-typed_arrays.js

export default function createInt8TypedArray(length, position, value) {
  const buffer = new ArrayBuffer(length);
  const int8View = new DataView(buffer);

  if (position >= length) {
    throw new Error('Position outside range');
  }

  int8View.setInt8(position, value);
  return int8View;
}
```

### Task 6: Set Data Structure

I created a function `setFromArray` that returns a `Set` from an array.

```javascript
// 6-set.js

export default function setFromArray(array) {
  return new Set(array);
}
```

### Task 7: More Set Data Structure

I created a function `hasValuesFromArray` that returns a boolean if all the elements in the array exist within the set.

```javascript
// 7-has_array_values.js

export default function hasValuesFromArray(set, array) {
  return array.every((value) => set.has(value));
}
```

### Task 8: Clean Set

I created a function `cleanSet` that returns a string of all the set values that start with a specific string (`startString`). The string contains all the values of the set separated by `-`.

```javascript
// 8-clean_set.js

export default function cleanSet(set, startString) {
  return [...set]
    .filter((value) => value.startsWith(startString))
    .map((value) => value.slice(startString.length))
    .join('-');
}
```

### Task 9: Map Data Structure

I created a function `groceriesList` that returns a map of groceries with the following items (name, quantity):

- Apples, 10
- Tomatoes, 10
- Pasta, 1
- Rice, 1
- Banana, 5

```javascript
// 9-groceries_list.js

export default function groceriesList() {
  const map = new Map();
  map.set('Apples', 10);
  map.set('Tomatoes', 10);
  map.set('Pasta', 1);
  map.set('Rice', 1);
  map.set('Banana', 5);
  return map;
}
```

### Task 10: More Map Data Structure

I created a function `updateUniqueItems` that returns an updated map for all items with initial quantity at 1. For each entry where the quantity is 1, the quantity is updated to 100. If updating the quantity is not possible (argument is not a map), the error `Cannot process` is thrown.

```javascript
// 10-update_uniq_items.js

export default function updateUniqueItems(map) {
  if (!(map instanceof Map)) {
    throw new Error('Cannot process');
  }

  map.forEach((value, key) => {
    if (value === 1) {
      map.set(key, 100);
    }
  });

  return map;
}
```

### Task 11: Weak Map Data Structure

I exported a const instance of `WeakMap` named `weakMap`. I also created a function `queryAPI` that tracks the number of times it is called for each endpoint. When the number of queries is >= 5, an error `Endpoint load is high` is thrown.

```javascript
// 100-weak.js

export const weakMap = new WeakMap();

export function queryAPI(endpoint) {
  if (!weakMap.has(endpoint)) {
    weakMap.set(endpoint, 0);
  }
  const count = weakMap.get(endpoint);
  if (count >= 4) {
    throw new Error('Endpoint load is high');
  }
  weakMap.set(endpoint, count + 1);
}
```

## Running Tests

I ran the following command to run tests and lint the project:

```bash
npm run full-test
```

## Conclusion

This project provided a comprehensive understanding of ES6 data structures and how to manipulate them effectively. Each task built upon the previous one, reinforcing concepts and improving my proficiency with JavaScript.
