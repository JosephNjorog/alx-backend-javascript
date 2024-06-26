# README

## Project: Promise Handling in JavaScript 

### Introduction
This project is a comprehensive practice in handling JavaScript Promises. Each task focuses on different aspects of Promises, such as creation, resolution, rejection, chaining, and handling multiple Promises. The exercises aim to solidify the understanding and effective use of Promises in asynchronous operations.

### Tasks

#### Task 0: Keep every promise you make and only make promises you can keep
**Objective:** Create a function `getResponseFromAPI` that returns a Promise.

**Steps:**
1. Implement the function `getResponseFromAPI` in the `0-promise.js` file.
2. Ensure the function returns a Promise that resolves with a simple response.
3. Test the implementation using the provided `0-main.js` file to verify the output.

**Outcome:**
- Successfully implemented a function that returns a Promise.
- Verified that the returned object is an instance of Promise.

#### Task 1: Don't make a promise...if you know you can't keep it
**Objective:** Create a function `getFullResponseFromAPI` that returns a Promise based on a boolean parameter.

**Steps:**
1. Implement the function `getFullResponseFromAPI(success)` in the `1-promise.js` file.
2. If `success` is true, resolve with an object containing status and body.
3. If `success` is false, reject with an error message.
4. Test using the provided `1-main.js` file.

**Outcome:**
- Function correctly resolves or rejects based on the boolean parameter.
- Promise resolves with a success object or rejects with an error message.

#### Task 2: Catch me if you can!
**Objective:** Create a function `handleResponseFromAPI` that handles a resolved or rejected Promise.

**Steps:**
1. Implement `handleResponseFromAPI(promise)` in the `2-then.js` file.
2. Append handlers to manage resolution and rejection.
3. Log a specific message in the `finally` block.
4. Test using the provided `2-main.js` file.

**Outcome:**
- Handlers correctly process resolved and rejected Promises.
- Log statement verifies the handling of a response from the API.

#### Task 3: Handle multiple successful promises
**Objective:** Handle multiple promises and log specific results or error messages.

**Steps:**
1. Import necessary functions from `utils.js`.
2. Implement `handleProfileSignup()` in the `3-all.js` file.
3. Use `Promise.all` to handle multiple promises and log results.
4. Handle errors appropriately.
5. Test using the provided `3-main.js` file.

**Outcome:**
- Successfully handled multiple promises and logged the appropriate results.
- Error handling ensures the correct message is logged when promises fail.

#### Task 4: Simple promise
**Objective:** Create a function `signUpUser` that returns a resolved Promise with user details.

**Steps:**
1. Implement `signUpUser(firstName, lastName)` in the `4-user-promise.js` file.
2. Ensure the function returns a Promise that resolves with user details.
3. Test using the provided `4-main.js` file.

**Outcome:**
- Function returns a resolved Promise containing the user's first and last name.

#### Task 5: Reject the promises
**Objective:** Create a function `uploadPhoto` that rejects a Promise with an error message.

**Steps:**
1. Implement `uploadPhoto(filename)` in the `5-photo-reject.js` file.
2. Ensure the function returns a rejected Promise with an error message.
3. Test using the provided `5-main.js` file.

**Outcome:**
- Function correctly rejects the Promise with the specified error message.

#### Task 6: Handle multiple promises
**Objective:** Handle multiple promises and return an array of results or errors.

**Steps:**
1. Import necessary functions.
2. Implement `handleProfileSignup(firstName, lastName, fileName)` in the `6-final-user.js` file.
3. Use `Promise.allSettled` to handle multiple promises.
4. Return an array of results and handle errors.
5. Test using the provided `6-main.js` file.

**Outcome:**
- Function handles multiple promises and returns an array with the status and value of each Promise.

#### Task 7: Load balancer
**Objective:** Create a function `loadBalancer` that returns the result of the fastest promise.

**Steps:**
1. Implement `loadBalancer(chinaDownload, USDownload)` in the `7-load_balancer.js` file.
2. Use `Promise.race` to return the result of the first resolved promise.
3. Test using the provided `7-main.js` file.

**Outcome:**
- Function returns the result of the fastest resolving Promise.

#### Task 8: Throw error / try catch
**Objective:** Create a function `divideFunction` that throws an error when dividing by zero.

**Steps:**
1. Implement `divideFunction(numerator, denominator)` in the `8-try.js` file.
2. Throw an error if the denominator is zero.
3. Test using the provided `8-main.js` file.

**Outcome:**
- Function correctly throws an error for division by zero and returns the division result otherwise.

#### Task 9: Throw an error
**Objective:** Create a function `guardrail` that handles errors and logs a message.

**Steps:**
1. Implement `guardrail(mathFunction)` in the `9-try.js` file.
2. Create an array to store results.
3. Append results or error messages and log a specific message.
4. Test using the provided `9-main.js` file.

**Outcome:**
- Function handles errors from the provided math function and logs a specific message.

#### Task 10: Await / Async
**Objective:** Handle asynchronous operations using `async` and `await`.

**Steps:**
1. Import necessary functions.
2. Implement `asyncUploadUser()` in the `100-await.js` file.
3. Use `async` and `await` to call the imported functions.
4. Return the results in an object or handle errors appropriately.
5. Test using the provided `100-main.js` file.

**Outcome:**
- Function correctly handles asynchronous operations and returns the expected results or an empty object on failure.

### Conclusion
This project provided practical experience in creating and managing JavaScript Promises, handling both successful and erroneous asynchronous operations. Through these tasks, various techniques and methods for Promise handling were explored, reinforcing the knowledge and skills necessary for efficient asynchronous programming in JavaScript.
