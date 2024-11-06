---
duration: 2h
---

# Lab: user local and application state, form manipulation

The state is central to any application. Multi-threaded applications access shared memory, distributed applications must choose between consistency and availability.

Web applications are no exception. The state is shared between the client and the server. In complex UI, clean and comprehensive state management is a key to robustness and enabling feature enhancements.

## Objectives

- Form manipulation
- State management in react

## Tasks

1. Component state (easy level)
2. Form with native elements (medium level)
3. Form with controlled elements (medium level)
4. Application state (hard level)

## Part 1. Component state (easy level)

Create a page with a counter increment when the user clicks on a button.

An initial page is available in ["/use_state"](http://localhost:3000/use_state). This exercise is directly inspired by the official[ React documentation on the state hook](https://reactjs.org/docs/hooks-state.html). Source your inspiration from there.

## Part 2. Form with native elements (medium level)

Create a login form with the `username` and `password` input and print its data when the user clicks on a button. You must use the `FormData` object to get the data contained in the form input elements.

An initial page is available in ["/login_native"](http://localhost:3000/login_native). 

## Part 3. Form with controlled elements (medium level)

Create a login form with the `username` and `password` input and print its data when the user clicks on a button. You must update a `data` object which is updated when the user enters some information inside the form elements. On submission, the `data` object must be filled with the value contained in the form elements.

An initial page is available in ["/login_controlled"](http://localhost:3000/login_controlled).

## Part 4. Application state (hard level)

A React context is provided in "/components/UserContext" to manage our user. It provides a `user` object, which is null when the user is logged out, as well as the `login` and `logout` functions.

1. Plug the exported context provider inside `/pages/_app.js`
2. In `components/Header.js`, import the exported `UserContext` and obtain the `user` object from the context API using the `useContext` hook
3. In `components/header/*`, make good usage of the `user` object and plug the `login` and `logout` functions into their respective `onClickLogin` and `onClickLogout` event functions.
4. Test it, when navigating across the pages, the "LoggedIn" and "LoggedOut" component states must be preserved.
