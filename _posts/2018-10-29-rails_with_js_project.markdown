---
layout: post
title:      "Rails With JS Project"
date:       2018-10-29 20:44:44 +0000
permalink:  rails_with_js_project
---

   Finally reached the end of Rails/JS and I couldn't be happier! Although the JavaScript portion of the curriculum seemed a lot shorter than the Rails section, I felt it was much harder to learn. I have the feeling that in programming, when learning anything new it is definitely going to be an uphill battle. The struggles that arose for me during JS, actually reminded me how much outside researching and learning has to be done on your own. When getting started with this project I did feel a sense of relief knowing that we were not starting from scratch. Being able to take the Rails projects we already created and build onto it was exciting. The first thing I realized thought was that I needed a better understanding of AJAX requests and events. This is when I found [Rose Weixel's tutorial on integrating Ajax with Rails](http://roseweixel.github.io/blog/2015/07/05/integrating-ajax-and-rails-a-simple-todo-list-app/). This was one of the very few tutorials I found that gave the option of not using `remote: true` and ending up being a great resource in completing this project. Key points/directions I found: 

##### Create Event Listener
1. Make sure document is ready `$(function()`
2. Listen for form submission `$("form").submit(function(e)`
3. Prevent the default behavior `e.preventDefault()`

##### Grab Form Info
1. Get action and method from form using `.attr()`
2. Pull values typed using `.find()` & `.val()`
3. Store values as variables

##### Make Ajax Request 
```
var data = $(this).serializeArray();

$.ajax({
  method: method,
  url: action,
  data: data
});
```
##### Handle the Response
1. Tell controller to respond to JS `respond_to`
2. Tell Ajax request to send back JS `dataType: 'script'`
3. Add file with path --> `app/views/<controller name>/<action name>.js.erb`
4. Create partial for displaying variable & render it in index page
5. Finally, in `create.js.erb`, render partial passing in local variable --> `$('ul').append("<%= j render partial: 'recipe', locals: {recipe: @recipe} %>");`






