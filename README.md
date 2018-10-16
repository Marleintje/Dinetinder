# Introduction

This 3-person group project contains a React App and was created in the 4th week of the Codaisseur academy. The React App was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).

## Initializing project

To view this project in a browser:
- Clone the project
- Run **yarn install** or **npm install** in the root folder of the project
- Run **yarn start** or **npm start** to run the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

## Project structure

The front-end is not connected to an API, and there is no backend and database, as we did not learn how to work with that yet in the 4th week of the academy. 

Instead, dummy-data has been saved in `src/reducers/reducer`. This dummy-data is used to set a part of the initial Redux state. Used input can be added via the website (e.g. *create profile* or *add dinner information*), and is added to the redux state via controlled components, actions and reducers. Note that refreshing the page will therefore set the redux state to its initial state with dummy data only.

## Project structure user-input example

An example on how user input is handled:

- When a profile is created, the user clicks on *Cooking dinner* and adds information. The information is saved in the component's local state by means of controlled components (`src/components/CookingContainer`);
- User clicks *Submit*. An action is fired with the user's information as an argument (`src/components/CookingContainer`);
- The action is dispatched with a shallow copy of the user's input as payload (`src/actions/user` --> addUser);
- The reducer 'reducer' catches the *addUser* action and concatenates the new user information with the existing array of users (`src/reducers/reducer`).