---
layout: post
title:      "The MVC Structure & My Real Estate App"
date:       2020-03-12 21:01:40 +0000
permalink:  the_mvc_structure_and_my_real_estate_app
---


In my last post, [Real Estate](https://nicaa0695.github.io/real_estate), I go over how I started building my real estate app. Since then, I've worked on more and I've mostly been adding CSS, bootstrap, and tweaking forms. I still have a ways to go but I'm happy with what I've got so far. 

While I was at Flatiron, I remember wishing time would slow down because we had so much to learn. At times, I would inevitably just have to make a few extra hours to focus on concepts I didn't quite grasp all the way. One of them was truly understanding how the MVC (Model, View, Controller) structure works. It's so important to understand it because once you do, building apps becomes much easier. 

In the curriculum, I remember it being compared to how a restaurant runs, with waiters, cooks, plates of food and so forth. After learning, here's my use of the MVC pattern in my real estate app. 

![MVC - Rails Architecture](https://miro.medium.com/max/916/1*KK61kGXrkaFBDfY7uWukyQ.png)

MVC is a design pattern that helps us organize our code so that we have a separation of concerns and someone could actually go in and be able to know exactly what is going on when they read through our app.  Basically, the browser sends a request to a web server that uses routes to figure out which controller to use. The controller then finds the correct view and interacts with the model which in turn interacts with the database and sends a response to the controller. Finally, the controller gives the output to the view based on the response. A little confusing, right? Hopefully once we break down what each component takes care of, things will become more clear.

The Model component contains the business logic, stores data, and communicates with the database. It is a Ruby class, for example: 

`class Property < ApplicationRecord`

  ` belongs_to :user`
	 
`end`

The Controller component interacts with both the model and the view. It interprets requests made by users and takes care of things like data submissions(when a user fills out a form), user sessions(when and how long a user is logged into an app), and cookies(data that a computer receives and then sends back without changing). Here's an example from my app of what a controller might look like with just a couple of methods so you get the idea:

`class PropertiesController < ApplicationController`

 ` before_action :set_property, only: [:show, :edit, :update, :destroy]`
 ` before_action :authenticate_account!, only: [:new, :create, :destroy]`

  `def index`
	
    `@properties = Property.all`
		
  `end`

 ` def new`
 
   `@property = Property.new`
	 
  `end`
	
`  end`

The View component contains things like HTML, CSS, JSON, etc. The view reads what it recieves from the controller but avoids getting involved with the logic. The show view generates the HTML which is what the user actually sees on their screen once everything is done. Here's an example of what a view might look like, in this case, a form for the user to fill out: 

`<%= form_with(model: property, local: true) do |form| %>`
  `<% render "layouts/validation", item: @property %>`

 `<div class="field">`
 
    `<%= form.label :address %>`
		
    `<%= form.text_field :address %>`
	 
  `</div>`

 ` <div class="field">`
 
    `<%= form.label :price %>`
		
    `<%= form.number_field :price %>`
		
 ` </div>`
 
 `<% end %>`
 
I had to spend some extra time really getting to know this pattern and I'm glad I did because the more I practice coding and building apps, the easier each one seems to be. Otherwise, everything would be so unorganized and we probably wouldn't enjoy coding as much as we do now. Even though software development is all about problem solving and mostly banging our heads against the wall, it's nice to have systems like this to help us focus on solving those problems, building apps quickly, and increasing productivity. Cheers to learning, growning, and coding!
 
 ![](https://www.salesforce.org/wp-content/uploads/2016/03/Girls-Who-Code.png)
 
 Peace, 
 
 Nica



