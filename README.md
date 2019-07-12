# Project

## TO-DO app

[click here for live version](https://fac-17.github.io/IJKL-week2-project/)

### Authors

- [@Coletterbox](https://github.com/Coletterbox)
- [@xIrusux](https://github.com/xIrusux)
- [@Albadylic](https://github.com/Albadylic)
- [@reubengt](https://github.com/reubengt)

## Description

A note taking app built using Test-Driven-Development.
Has functionality to add and remove notes, and mark them as 'done'.

## User stories:

As a disorganised person I want to:

- enter tasks I need to do into a web page so that I don't forget them
- view the tasks I have added in a list so that I can plan my day
- mark tasks as complete so that I can focus on the tasks I have left
- the to-dos to be large enough so that I don't hit the wrong one with my thumb

#### Potential stretch goals

As a disorganised person I want to:

- edit my to-dos so that I can amend them if the task changes
- click on any part of a to-do to mark it as complete so that it's easier for me to check to-dos off
- a visual indication of which to-do I'm about to interact with so that it's clear what I'm editing

## Main Goals/Build Process

The process is split into three parts:

#### 1. Using TDD to create the logic needed to modify our to-do list. This involved writing three functions.

**addTodo**

- Add to-do takes two arguments, a to-do array and a to-do element. The to-do element may be missing some of the data that a to-do needs.
- if either 'description', 'id' or 'done' attributes are missing, they need to be added in.
- id should be generated by calling generateId()

**deleteTodo**

Add to-do takes two arguments, a to-do array and a to-do element. It removes the to-do element from the array (the reverse of addTodo).

**markTodo**

markTodo marks as to-do as completed.

#### 2. Render the to-do list to the DOM

User input is processed as todo objects inside a todo array, then populated inside a list on the page.

**TO-DO objects are objects with three properties: id, description, done.**

`{ id: 0, description: 'smash avocados', done: true, }`

**TO-DO array is a collection of TO-DO objects**

`[ { id: 0, description: 'smash avocados', done: true, }, { id: 1, description: 'make coffee', done: false, }, ]`

**User Input to the text field is dealt with in the following ways**

- a todo object is created from the user input, this will contain all necessary attributes(an event listener is added to the submit action, and todoFunctions.addtoDo() is used to create a todo object from the user input)
- this object is converted to a list item in the createTodoNode() function.
- the list item is added to an unordered list containing all the todos, using the renderState() function.

#### 3. Adding our own features

Styling the page! Making it visually seductive :D

## Problems we had

- Forgetting to branch
- Understanding the skeleton we were given
- Understanding that the DOM is rendered and then remains static. This meant we were complicating our addition of a tick to the button when a todo was marked done. In the end, this was as simple as adding an if statement to check if done === true.
- When writing tests we used a static set of data. Some simple tests succeeded but would break when we refactored our code. In order to overcome this we could have used unique data per test (Thanks, Jan).

## Things we learnt

- How to manipulate the DOM
- The DOM is rendered and if it is changed, it must be updated!
- Callbacks
- Cloning an array/object allows you to manipulate it and leave it unchanged
- How to use git stash to prevent master conflicts when forgetting to branch

## Issues addressed

- Cleaning up console logs / formatting functions / housekeeping
- Compressing background image
- Don't allow submissions of empty fields and clear field when submitted
- Fix accessibility from 60 - 100!
- Converting ES5 => ES6
