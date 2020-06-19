---
layout: post
title:      "IG Clone in Ruby on Rails"
date:       2020-06-19 20:21:38 +0000
permalink:  ig_clone_in_ruby_on_rails
---


**Feeling like I'm on a merry-go-round**

![](https://i.pinimg.com/originals/d2/f1/46/d2f146fd51b667f6da1d39e945ebb41b.gif)

And not in a fun way.

Hey folks! I wanted to talk a little bit about what's been going on in my world lately. I'm still on the hunt for a position. I had a first-round interview that was supposed to lead to a second interiew (everything went well and we seemed to be a match). However, before I got the chance to have the second interview, they decided to go with another candidate who closely matched what they were looking for at this time. Congrats to that person but BOO! 😭 I will admit, I'm feeling super discouraged right now. I feel like I'm doing so much to continue learning and growing and it doesn't seem to be getting me anywhere. I guess all I can do is keep trying. To anyone out there who is searching, keep your head up! This can't last forever. WE'VE GOT THIS. 💪🏻 

**Goals**

I have a few goals set, one is completing my AWS cert within the next couple of weeks. Second, I am going to make some changes to my resume and project walkthroughs in hopes that hirig managers are more inclined to take a look. And third, I'm also working on a new project; an instagram clone. Half of it will be coding along and half of it will be implementing my own features for extra practice and fun. I use instagram on a weekly bases so I figured why not build my own version. It will be another great opportunity to learn or reinforce a few things! I decided to use Ruby on Rails because that's what language I'm most interested in as far as a career. 

**Lets jump in**

As most of you may know, Instagram is an app that allows you to make an account, follow/gain followers, post photos and/or videos on your profile page as well as onto your "story". From there, people can "like" or comment on your content. There's also a personal messaging feature on there that we won't get to right away but hopefully will soon. Like I said, I will be using Ruby on Rails and the Bootstrap CSS Framework for styling. It's great for moving along faster and it looks fantastic. I'm using it because I could use some practice. I want to incorporate most or all of these features but also throw my own style and spin in there. We will just see where we go! 

**Github Repo**

* To start, I created a new repository on Github. 👉🏻 [Github.com/new](http://github.com/new) (make sure you have a Github account)
* I named my repository "igclone" but you can name it whatever you'd like.
* I left all the default options alone and clicked "Create Repository".
* Then, I copied the SSH link that we will use soon.

**VS Code**
* In my terminal, I created a directory for my project. 👉🏻 `mkdir igclone`
* I cd'd (change directory) into my new repo. 👉🏻 `cd igclone`
* Created a README.md file. 👉🏻 `touch README.md` - This is where you'll want a brief description of your project as well as instructions on using it and technologies used.
* Initialize empty git repo. 👉🏻 `git init`
* Add our README.md file. 👉🏻 `git add README.md`
* Commit our file. 👉🏻 `git commit -m 'initial commit'`
* Set up push destination. 👉🏻 `git remote add origin [SSH code we copied earlier]`
* Push the code to the repo. 👉🏻 `git push -u origin master`
* Create new branch for development. 👉🏻 `git checkout -b [development]` When you're working on the development branch and all your code works and youre happy with it, you can merge in with the master branch. 👉🏻 `git checkout master`, then `git merge development`, then commit changes from master branch `git add .`, `git commit -m 'commit message'`, `git push`

Now we can push your code up to github when needed and begin building our app! 

We can use `rails new igclone` to set up our application, download all the required gems and create all the files we will use! Easy right? Now when we run `rails s` and go to http://localhost:3000/, we see:

![](https://sahilthakur7blog.files.wordpress.com/2017/11/rails-splash-page.jpg?w=648)

I think that's all we will cover today. Meanwhile, I'll be working on the app some more and be back with my steps next week. I hope everyone has a nice, relaxing weekend. Happy Father's Day! 

Peace, 

Nica



