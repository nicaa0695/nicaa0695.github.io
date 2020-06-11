---
layout: post
title:      "Ruby Scope"
date:       2020-06-11 17:36:53 -0400
permalink:  ruby_scope
---


Hi everyone! Let me just start by saying if you haven't gone on a camping trip recently, you should! We went to Haviland campground near Durango, CO for our anniversary and it was so nice to get away. We went kayaking, hiking, and met a few cool people that were camping near us. Even though I code everyday, it was nice to not be on my computer or phone for almost 5 days. I was able to read and just enjoy nature while forgetting about everyday's tasks. Now I'm back and ready to code and continue the job search. I've had a couple phone interviews that I feel have gone pretty well and I'm hoping one of them turns into a job opportunity. Besides that, this week I've made some great connections on LinkedIn that have given insight as to what their experience at their company has been like and ideas of what their interview process looked like. Recently, I've had lots of meaningful conversations and feel like it's just a matter of time before I get my one "YES!". Let me tell you, it's been tough hearing so many "no's". I've been focusing on practicing cultural interview questions and studying for technical interviews as well. 🤞🏻 Let's jump into scope in Ruby!


**Variables**

If you've read my previous blog posts, you know that different types of variabes are written as follows:

1. Local Variable - `variable`
2. Instance Variable - `@variable`
3. Class Variable - `@@variable`
4. Global Variable - `$variable`


**Why is scope important?**

It's important to understand scope, not just in Ruby, but in any programming language. When coding, you're bound to run into errors that may come from not understanding scope. Once you take the time to undersnad it, you can solve those errors with ease or just avoid them entirely. 😁👍🏻 Some errors you might run into as a result of not understanding scope: 

1. Say you wanted to see an array of all the people in a class. You would want to be able to say, `Person.all` but you'll get this error: 
`undefined method 'all' for Person:Class`
To fix this, you'll need to build a class method because you were trying to call the 'all' method on the Person class itself. 
```
def self.all 
   @@all       👈🏼#here we are in the class scope!
end
```

2. Say you wanted a basketball player to be able to dribble. You would want to be able to say, `kobe.dribble` but you will get this error: 
`undefined method 'dribble' for #<Person:0x007st74bfw02`
To fix this, you'll need to build an instance method because you were trying to call the 'dribble' method on an instance of the Person class.
```
def dribble
   puts "The person is dribbling a basketball."   👈🏼#here we are in the instance scope
end
```

**Hoisting**

Remember everything in Ruby is an object, even scopes! When Ruby parses a file, it ‘hoists’ each variable to the top of its scope, declaring and setting it to `nil`, even if that variable is never assigned in our code.

**You can always go up👆🏻 the scope chain, but not down.👇🏻**

Meaning classes **can't** access instances and instances **can't** access local.

But local **can** access instance scope and instances **can** access class scope!

Here's a visual I found on google to make it a little easier to understand: 

![](https://www.natashatherobot.com/wp-content/uploads/variable-scope-ruby.jpg)



I wanted to go over scope because when I first began coding in Ruby, I would get these errors and even though they are telling you exactly what to do to resolve the issue, it can be difficult if you don't quite understand the concept. Hopefully this was helpful, see you guys next week! 👋🏻

Peace, 

Nica
