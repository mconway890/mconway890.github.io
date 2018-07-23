---
layout: post
title:      "Rails Portfolio Project"
date:       2018-07-23 21:41:02 +0000
permalink:  rails_portfolio_project
---


For my rails project I decided to create a Recipe Manager as suggested in the lesson called "Veggie Recipes". As a vegetarian I thought it would be great to have a place to store all my recipes along with my own reviews and difficulty rating for each. I started by setting up all the necessary folders and views and then dove deeper into the nested routing and associations once the structuring was complete. The project became difficult as I progressed, especially when dealing with the associations. With the help from several technical coaches and utilizing [Gliffy](https://www.gliffy.com/), I was able to correct the relationship between my recipe and ingredients models. The next problem I encountered was adding a third party signup. My app uses Devise which can be so helpful and yet so destructive if set up or used the wrong way. When trying to add a third party signup, I tried everything from Facebook, Google, Github and Twitter and nothing seemed to work when paired with Devise. After a lot of stack overflow research and more coach help, I finally fixed the authentication issue and was able to have Devise and Facebook Login work together. Another issue I encountered turned out to be an HTML issue. When setting up one of my form partials, I decided to nest it inside of a `<table>` for styling purposes. The form looked great in the view, however after more research I discovered that nesting `form_for` inside of a `<table>`, will cause your submit button to stop functioning therefore never submitting your form. By undoing these changes and reverting back to the original styling I had, the submit button started to work. 

As the curriculum progresses, I've definitely seen how much more intense the projects get but it's also a great way to see how much I've learned already and that makes me hopeful.
