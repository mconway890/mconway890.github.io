---
layout: post
title:      "React Redux Project - Beer Fridge"
date:       2018-11-16 15:43:32 +0000
permalink:  react_redux_project_-_beer_fridge
---


![It's done.](https://media.giphy.com/media/3oKIPf3C7HqqYBVcCk/giphy.gif)

I started the online program with Flatiron back in August of 2017. At the time I had just finished several months of courses through [Codecademy](https://www.codecademy.com/) and other online schools and thought I'd be able knock out the curriculum within about six months. Upon starting I was eager and excited and able to put in the eight hours a day that I had planned on. However, a couple of months in and my timeline started to change. As the labs intensified and each lesson become more intricate than the last, I realized my schedule had to change in order to retain the information efficiently. I also realized how important outside research is when learning to program and how self-sufficient you need to be. By utilizing the learn videos, slack channels, study groups and coaches, I finally made it to the final project.

For my React Redux Project I decided to make a Beer Management System. I used `create-react-app` to get started, and in a seperate repo using `rails new`, I set up my back end api. In my api I created a Beer model, serializer and generated migrations. For my controller, after some research I found that using `app/controllers/api/v1` and nesting the controller in a module, is a good practice to avoid breaking changes and provide some backwards compatibility with the API. Next I added beers as a resource in `config/routes.rb` in addition to some seed data. I then created a client folder to house the react directories and merged my api with my react app.

For my front end, I began by adding routes to the default page utilizing `react-router-dom`. I then added a NavBar, Home, Contact, About and BeerCard component. The BeerCard component would be used to render the attributes submitted through the input form when creating a beer. In my containers directory, I added BeerInput which handles the change and submit events of the form. In my reducers and actions I added case statements for adding, removing, upvoting and downvoting beers along with fetch requests to GET and POST data from the API. Finally in my containers, I added a Beers component that renders the table of beers that have been created along with the option to like and dislike a beer. 

For the final product being a single page application I thought the process would be a bit quicker, and yet I have made nearly 200 commits. I look forward to adding to them along with all my other projects I've made through Flatiron because if I've learned anything, it is that your work is never reall done.

> "Every great developer you know got there by solving problems they were unqualified to solve until they actually did it." - Patrick McKenzie
