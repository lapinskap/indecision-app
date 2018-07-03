# Indecision App 
React App created with Andrew Mead course. ToDo based application to store ideas in local storage.


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

![Example screenshot](https://raw.githubusercontent.com/lapinskap/lapinskap.github.io/master/assets/img/projects/proj-1/thumb.jpg)


![Example screenshot](https://raw.githubusercontent.com/lapinskap/lapinskap.github.io/master/assets/img/projects/proj-1/dog.jpg)

![Example screenshot](https://raw.githubusercontent.com/lapinskap/lapinskap.github.io/master/assets/img/projects/proj-1/wall.jpg)

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

##### SCSS
Another styles for mobile devices

| [file path](./src/styles/components/)     | 
| :---------------------------------:|

```sass
//for non-mobile devices
@media (min-width: $desktop-breakpoint) {
    .big-button {
        margin-bottom: $xl-size;
    }
}

@media (min-width: $desktop-breakpoint) {
    .header {
        margin-bottom: $xl-size;
    }
}
```

Application on the phone looks as follows:

![mobile](https://raw.githubusercontent.com/lapinskap/lapinskap.github.io/master/assets/img/projects/proj-1/mobile.jpg)

##### React Modal
small window which pushes up while clicking "What should I do" button

| [file path](./src/components/OptionModal.js)     | 
| :---------------------------------:|


```javascript
import React from 'react';
import Modal from 'react-modal';

const OptionModal = (props) => (
     <Modal
     isOpen = {!!props.selectedOption}
     contentLabel="Selected Option"
     onRequestClose={props.handleClearSelectedOption}
     closeTimeoutMS={600}
     className="modal"
     >
        <h3 className="modal__title">Selected option</h3> 
        {props.selectedOption && <p className="modal__body">{props.selectedOption}</p>}
        <button className="button" onClick={props.handleClearSelectedOption}>Okay, fine</button>
     </Modal>
 );


export default OptionModal; 
```

I highly recommend also to look into the [playground folder](./src/playground/) - it shows which things I had to practice to understand the implementation thoroughly. To do those exercises I was using mainly documentation. There is a version of the application written in JSX.




## Features

* SCSS (RWD)
* Ecmascript 6 syntax
* Webpack.config.js file
* Stateless function components
* Props and State
* BEM naming convention

## Status
Project is: _finished_

## Inspiration
Project based on Andrew Mead React Course which I catched on Udemy.com.


andrew mead app deploy: https://budget-app.mead.io/
