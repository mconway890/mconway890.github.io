---
layout: post
title:      "Sinatra Portfolio Project"
date:       2018-02-05 13:07:38 -0500
permalink:  sinatra_portfolio_project
---


For my Sinatra Portfolio Project I wanted to create something fun and engaging that I knew would keep my focus. After being in the online web program for about five months now, I realized in order to stay motivated on a project I had to have an interest and passion in what I was making. I started the project by doing some research online. I read former blogs on  projects that had been done before and ultimately decided on making a Fantasy Quidditch site. (*I knew this would keep me engaged due to my irrational obsession with all things Harry Potter* ) For those unaware of the sport, [Quidditch](https://en.wikipedia.org/wiki/Quidditch) is a game played by two teams mounted on broomsticks as featured in the worldwide film/book phenomenom "Harry Potter". With the Super Bowl approaching and the overall excitement and fascination people have in fantasy leagues, I thought this would be a fun and comical idea. 

I started the project by creating my models - My Team model which belongs to a User, and a User model which has many Teams. Next, I decided how many controllers I would have. The Fwitter lab helped with this decision because it was there that I realized having multiple controllers helps tremendously with organization and overall readability of your routes. I created an application controller, a team controller and a user controller. I then began setting up my routes and erb view pages. In addition I added a folder titled helpers that would hold my ruby helper methods. 

The homepage of my app is very basic. It welcomes you to Fantasy Quidditch and presents two buttons - Login & Signup. If login is unsuccesful you are led to a login error page and the same goes for a signup error. With a succesful login you are taken to the teams index and can continue editing/deleting/creating your teams. From signup you are then prompted to login and led the same route. Users must be logged in to edit or delete a team and they must be the original team creator. In addition, users may view teams made my by other users, without the ability to revise them.

My favorite part of this project was seeing the code come to life in a functioning website created from scratch. With so many labs and lessons in this course based on tests or codealongs, It was refreshing to create something unique and imaginative with total flexibility. It was fun being able to create each aspect of the site and especially having the chance to use HTML and CSS again. 

[Fantasy Quidditch!](https://github.com/mconway890/sinatra-portfolio-project)
