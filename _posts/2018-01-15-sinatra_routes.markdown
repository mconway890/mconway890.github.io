---
layout: post
title:      "Sinatra Routes"
date:       2018-01-15 21:38:53 +0000
permalink:  sinatra_routes
---


It has been quite some time since my last blog entry so today I decided to tackle that **PAST DUE** memo that's been haunting me on my homepage. I've always enjoyed writing whether it be for pleasure or academic purposes, however when it comes to writing about code I find my confidence is lacking. It has been five months since I began the online course with Flatiron and I feel I've made great progress. There are some weeks that are more productive than others but overall I feel I've learned a tremendous amount. I think the more I talk about what I learn and try and teach others as well, the more confident I will be in my writing. I am quickly approaching my second project (Sinatra Portfolio Project) with only one lab to go. The lab I am currently on, "Fwitter", has been giving me many issues. The main struggle I have had thus far with Sinatra, is understanding it's routes and how they work. After writing each route required for this lab in the application controller and still getting zero passing tests, I decided to do some research to try and further my understanding. 

Prior to Flatiron's online course, I was learning to code through [codecademy](https://www.codecademy.com/learn), [w3schools](https://www.w3schools.com/), and several other coding tutorial sites. I decided to revisit some of these to gain a better understanding of how Sinatra routes work. The following are some of my findings that I found helpful:

* Sinatra reads the routes in the order they’re written in your Ruby file; as soon as it finds a route that matches the request sent to the server, it executes that route. This means that routes should be listed in order from most specific to least specific.

```
get "/:everything" do
  "I match everything typed in the URL after '/'!"
end

get "/partytime" do
  "This is a super exciting block, but it will never execute, because the first 'get' route matches '/partytime'."
end
```

* In Sinatra, a route is an HTTP method paired with a URL-matching pattern. Each route is associated with a block.
*  Routes are matched in the order they are defined. The first route that matches the request is invoked.

```
get '/' do
  .. show something ..
end

post '/' do
  .. create something ..
end

put '/' do
  .. replace something ..
end

patch '/' do
  .. modify something ..
end

delete '/' do
  .. annihilate something ..
end

options '/' do
  .. appease something ..
end

link '/' do
  .. affiliate something ..
end

unlink '/' do
  .. separate something ..
end
```

* Each template language is exposed via its own rendering method. These methods simply return a string:

```
get '/' do
  erb :index
end
```

* The above code renders views/index.erb.

> "...you have to constantly plan for and design around your inevitable human mistakes and fallibility"                                                                                - Jeff Atwood, Coding Horror
