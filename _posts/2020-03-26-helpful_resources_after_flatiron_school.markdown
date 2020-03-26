---
layout: post
title:      "Helpful Resources After Flatiron School"
date:       2020-03-26 18:27:11 +0000
permalink:  helpful_resources_after_flatiron_school
---


In last week's post, [Job Hunt, Coding, and Chaos](https://nicaa0695.github.io/job_hunt_coding_and_chaos), I talked about how I hadn't worked on my app much. I made a few changes to it but I was more focused on reading and watching video tutorials. I found a YouTuber awhile back whose channel is called Traversy Media. He has a wide range of videos from crash courses, actual courses, code-alongs, and tutorials. He covers several languages including JavaScript, Node.js, Python, Ruby on Rails and so many more. He's been very helpful for me as far and Ruby and JavaScript, not only does he have courses on these languages but he also does shorter tutorials for concepts you may be having trouple understanding. If you are stuck on certain topics, you can find him here: [Traversy Media - YouTube](https://www.youtube.com/user/TechGuyWeb) or at his website where he has courses ranging from 6-21 hours - [traversymedia.com](https://www.traversymedia.com/). The book I bought, Cracking the Coding Interview, has been pretty helpful too, it has over 150 interview questions, strategies to take on algorithms and getting to answers on your own when you ask the right questions, and even tips for non-technical questions that might come up. I've read and worked through about a quarter of the book, it can be exhausting but really beneficial if you're currently searching for a job like I am. And like I mentioned last week, [HackerRank](https://www.hackerrank.com/) and [CodeWars](https://www.codewars.com/) are also awesome for working on code challenges!

![](https://www.memecreator.org/static/images/memes/5024322.jpg)

This week, I have gotten to work on my Real Estate app and I feel like I'm pretty close to being done. I've implemented more bootstrap and it looks pretty good, probably my best project yet. However, I keep running into issues with Devise and my login system. When a user signs up and logs in, nothing happens! After clicking 'login' , I check the logs and there are no changes. I'm not sure if a request is not being sent or if it's a problem with the turbolinks gem like I've run into in the past. If it is turbolinks, which makes navigating your web application faster, I will have to (1.) remove it from my Gemfile:

`gem 'turbolinks', '~> 5',` 

(2.) Run `bundle install` 

and (3.) in app/views/layouts/application.htm.erb, set turbolinks to false: `<%= stylesheet_link_tag 'application', media: 'all', 'data-turbolinks-track' => false`



In next week's blog I will write about how I fixed the problem, hopefully it's a silly typo somewhere or a small change like this I need to make that I'm just not seeing right now. I've also finally added actual instances of properties on the home page in place of the dummy text so now users can actually go in and add properties for sale or browse through properties to buy. I used the [carrierwave gem](https://github.com/carrierwaveuploader/carrierwave) in my app to allow users to upload photos of the properties. Now I need to make some tweaks to get my CSS and HTML to get things looking more professional, add icons with [Feather Icons](https://feathericons.com/) so the app is more user friendly and make sure that properties can only be edited or deleted by the person who created them. 

![](https://i.chzbgr.com/full/6347654144/h57FD7BDD/almost-there)

I should be able to have it complete by the middle of next week and then I can work on deploying it. If I finish as planned, maybe in next week's post I will talk about deploying the app to the web with [Heroku](https://www.heroku.com/) in addition to discussing how I solved my issue with Devise.

Peace,

Nica


