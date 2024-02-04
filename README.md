# Todo Application - JUnit Testing

## Introduction

Welcome to the Todo Application JUnit Testing README! This document helps you understand how we test our Todo Application using JUnit. JUnit is like our superhero that checks if everything in our code works as expected.

## Understanding JUnit Testing
### What is JUnit?
JUnit is like a helpful friend for programmers. It helps us make sure our code is doing what it's supposed to do. Imagine you're building a robot, and JUnit is your assistant checking if every part of the robot works correctly.

### Why do we need JUnit?
Imagine you're baking cookies. Before serving them to your friends, you want to make sure they taste good. JUnit does something similar for our code – it tastes our code and tells us if everything is working fine.

### Writing Tests
Writing tests is like making a to-do list before you start baking cookies. You list what the cookies should taste like, and then you check if they really do.
In JUnit, we write tests to check if our code works as expected. We create scenarios like, "If we give the robot this command, does it do what we expect?"

### Test Cases
A test case is like a single item on your to-do list. Each test case checks one specific thing. For example, one test case might check if the robot can move forward, and another might check if it can turn left.

### Assertions
Assertions are like statements you make about your cookies. "The cookies should be sweet." In JUnit, assertions are the statements we use to check if our code behaves the way we expect.

### Running Tests
After writing our to-do list and making our statements, it's time to run the tests. This is like putting the cookies in the oven. We see if everything comes out as expected.

### Green and Red Lights
When all tests pass, it's like getting a green light – everything is good. If a test fails, it's like a red light, signaling something needs fixing. JUnit shows us these lights to help us know if our code is ready to share with others.

### Refactoring
Refactoring is like upgrading your recipe. JUnit helps us feel confident that even after changing our code, it still works as expected. It's like testing if the new cookie recipe is still tasty.

### Continuous Testing
Imagine having a friend taste every batch of cookies you bake. Continuous testing is similar; it's like having JUnit check our code automatically every time we make a change. This way, we catch any issues early on.


## Testing Environment

We set up a special place called the "Testing Environment" using some tools:

- **SpringBootTest:** This tool helps us test different parts of our Todo Application.
- **MockMvc:** Imagine this like a pretend internet for our app. We use it to make sure our app's web part works correctly.

## Test Packages
### 1. TodoServiceJUnitTest
This package is like a box of tests for the service part of our app. We check if we can get a list of todos, find a todo by ID, and handle cases when the ID is not right.

### 2. TodoControllerJUnitTest
This box of tests is for the internet part of our app. We check if we can get all todos and create a new one using the REST API.

## Test Descriptions

### TodoServiceJUnitTest
1. `whenFindAll_ReturnTodosList`
Description: We check if our app can give us a list of todos.
Test Scenario: We tell our app to give us some pretend todos, and we check if it gives the right ones.

2. `whenGetById_TodoShouldBeFound`
Description: We test if our app can find a todo using its ID.
Test Scenario: We tell our app to find a todo with a special ID, and we check if it finds the right one.

3. `whenInvalidId_TodoShouldNotBeFound`
Description: We check what happens when we ask our app for a todo with an invalid ID.
Test Scenario: We ask our app for a todo with a pretend invalid ID and make sure it says it doesn't exist.


### TodoControllerJUnitTest
1.` whenGetAllTodos_thenReturnJsonArray`
Description: We test if our app's internet part can give us a list of todos.
Test Scenario: We tell our app to pretend it's on the internet and ask for todos. We check if it gives us the right ones in a special format.

2.` whenPostTodo_thenCreateTodo`
Description: We check if we can tell our app to make a new todo.
Test Scenario: We ask our app to create a new todo, and we check if it says, "Okay, I did it!" and gives us the new todo.
