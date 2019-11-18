---
layout: post
title:      "Project 4 - Rails API with JS frontend"
date:       2019-11-18 02:13:06 +0000
permalink:  project_4_-_rails_api_with_js_frontend
---


As I *finally* complete project 4, Rails API with JS frontend, I can say that was by far the hardest assignment for me so far. The front end set up was easier because I'm much more comfortable with Rails than JS. The backend took me probably two hours total. The frontend was the hard part and I think it was because it felt like we had a lot less time to learn Javascript. Also, the concepts in my opinion are just a lot harder to grasp; I definetely need to keep practicing. My cohort lead said something that relieved some of my nervousness: People typically enjoy React because it takes care of some issues you might run into with vanilla JS. 
One issue I ran into while working on this app was the rack-cors gem and Cross-Origin Requests. After I installed the gem 'rack-cors', there was some code that needed to be commented out in config/initializers/cors.rb: 

`Rails.application.config.middleware.insert_before 0, Rack::Cors do
  allow do
    origins '*'

    resource '*',
      headers: :any,
      methods: [:get, :post, :put, :patch, :delete, :options, :head]
  end
end`

I made the silly mistake of leaving "example.com" where the "*" should've been, like so: 
```
Rails.application.config.middleware.insert_before 0, Rack::Cors do
  allow do
    origins 'example.com'

    resource '*',
      headers: :any,
      methods: [:get, :post, :put, :patch, :delete, :options, :head]
  end
end
```

So if you're running into issues with fetch, that might be a good place to look.

Another issue I had was an error in the terminal when trying to add a chore: 
```
ActiveRecord::StatementInvalid (SQLite3::BusyException: database is locked):
  
app/controllers/chores_controller.rb:15:in `create'
```
This may indicate that you have DB Browser for SQLite and rails console running simultaneously. That took me a long time to figure out because that was just one of many things that could've been wrong.

Overall, I feel a little better about JS but as I said before, I need lots of practice and I'm looking forward to React and finishing off the program strong! 

# One more month!!!
