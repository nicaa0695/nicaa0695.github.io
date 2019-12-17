---
layout: post
title:      "Final Project for Flatiron School"
date:       2019-12-16 19:53:45 -0500
permalink:  final_project_for_flatiron_school
---


I've finally completed my final project for Flatiron! I love traveling so I decided to make an application for other people who love it as well. This project was built with a Rails API and a React/Redux frontend and it was a tough one for me. Before starting, I had to review several concepts. After reviewing, I wrote out my ideas on paper. I drew out how I wanted everything to be structured, and made sure I was (mostly) organized before starting. I completed the backend quicker than the frontend because I'm much more familiar with Ruby on Rails than JS. But, I got through it and I'm super stoked about what I built.

In the app, you can add destinations with a city, country, and image URL. You can add activities to those destinations as well as add destinations to your bucket-list or to a list of places you've been to.

Two areas, Props and State, took me some time to grasp and still aren't the easiest for me. 
So what is state? It's an object that represents the parts of the app that can change. Each component can maintain its own state, which lives in an object called `this.state`.
And what are props? Props are used to pass data from a parent component to a child component in React and they are the main mechanism for component communication. 
Your project will go a lot smoother once you take the time to understand these concepts as best you can!

Another thing I got to fully understand was using Thunk which is a middleware that lets you call action creators that return a function instead of an action object. That function receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the body of the function once the asynchronous operations have completed. 
```
import { createStore, applyMiddleware, compose } from 'redux';
import thunk from 'redux-thunk';
let store = createStore(destinationReducer, composeEnhancers(applyMiddleware(thunk)));
```

I want to list a few things that helped get me through building this project.
1. React/Redux dev tools and debugger; are your friends!
2. Short YouTube videos explaing anything I didn't quite understand. (because I learn better with visuals)
3. Re-reading Read-Me's (say that 10 times fast) or any hepful articles you find on the web.
4. Be patient with yourself, take breaks when needed.
5. [Click Here for an Article on Understanding State in React](https://medium.com/the-andela-way/understanding-the-fundamentals-of-state-in-react-79c711be677f)
6. [Click Here for an Article on Props and State](https://medium.com/@decode2018/props-vs-state-react-64fcf6c55886)

I did more styling on this project than on previous projects. CSS is not the easiest for me but it sure makes a huge difference when trying to show off your project so I decided to work harder at this, this time around. Simple google searches when I got stuck were ultimately what saved me, especially when I wanted something to look a certain way(before I could move on because I'm a little crazy).

Here is a video walkthrough of my project: [Travelers](https://www.youtube.com/watch?v=Riye1tGhxa4&t=41s)

I'm so excited to have finished the final project! Now I get to move on to the job search which means perfecting my resume and reviewing, reviewing, reviewing to be interview ready!!! 





