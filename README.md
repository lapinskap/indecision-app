# Indecision App 
React App created with Andrew Mead course, contains SCSS and own webpack.config.js file


## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)


## General info
"Indecision App - Put your life in the hands of a computer" - React ToDo app which stores your options in local storage. For this purpose application contains react Props and State (JSON). No real database provided.

I implemented SCSS for the first time here + it is my first RWD experience (I added another styles for mobile devices)
The playground folder contains simple jsx and es6 scripts, mainly the methods that I've learned to build more complex applications.

I wrote my own webpack file configuration for the first time. It was necessary to use SCSS (instead of CSS) in the project.


## Screenshots

![Example screenshot](https://raw.githubusercontent.com/lapinskap/lapinskap.github.io/master/assets/img/projects/proj-2/add.jpg)


![Example screenshot](https://raw.githubusercontent.com/lapinskap/lapinskap.github.io/master/assets/img/projects/proj-2/stretch.jpg)

![Example screenshot](https://raw.githubusercontent.com/lapinskap/lapinskap.github.io/master/assets/img/projects/proj-2/thumb.jpg)

## Technologies
* JavaScript - Ecmascript 6
* SASS - SCSS preprocessor
* Node modules [(see dependencies in package.json)](./package.json)
* React - JavaScript library

## Setup
To run this project, install it locally using yarn:

```
$ cd ./indecision-app
$ yarn install
$ yarn run dev-server
```
Alternatively you can use npm:

```
$ cd ./indecision-app
$ npm install
$ npm run dev-server
```

## Code Examples

###### Simple Header component created with fat arrow function - contains React Router

| [file path](./src/components/Header.js)     | 
| :---------------------------------:|

```javascript
const Header = () => (
    <header>
        <h1>Expensify</h1>
        <NavLink to="/" activeClassName="is-active" exact={true}>Dashboard Page </NavLink>
        <NavLink to="/create" activeClassName="is-active"> Create Expense</NavLink>
        <NavLink to="/help"  activeClassName="is-active">Help Page</NavLink>
    </header>
    );

export default Header;
```

> With React’s stateless functional components, each component can be easily tested in isolation. No mocking, state manipulation, special libraries, or tricky test harnesses are needed.

###### ![Reducer](https://redux.js.org/api-reference/combinereducers) example - catches log in and log out actions - contains Redux

| [file path](./src/reducers/auth.js)     | 
| :---------------------------------:|


```javascript
export default (state = {}, action) => {
  switch (action.type) {
    case 'LOGIN':
      return {
        uid: action.uid
      };
    case 'LOGOUT':
      return {};
    default:
      return state;
  }
};
```

## Features

* React Router
* Redux
* Firebase
* Jest
* Enzyme
* SCSS
* Ecmascript 6

## Status
Project is: _finished_

## Inspiration
Project based on Andrew Mead React Course which I catched on Udemy.com.


andrew mead app deploy: https://budget-app.mead.io/
