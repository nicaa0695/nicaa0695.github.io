---
layout: post
title:      "Object Oriented Ruby pt. 3 "
date:       2020-04-16 23:18:49 +0000
permalink:  object_oriented_ruby_pt_3
---


Let me just start out by saying, "WOW, what a year April has been!" 

![](https://golfshot.com/wp-content/uploads/2019/03/bcf.png)

It's getting really hard to stay inside all of the time. All I have to say is thank goodness for take out food and Home Depot. Don't get me wrong, I enjoy cooking but I want to go to a restaurant to have a beer, a steak and to see my friends and family!

![](https://img.ifunny.co/images/1c0217ade5a4f22f158a668c9d453ef5864b6c9051e904dc9ca86f294b4740d3_1.gif)

This week, I've been spending a lot of time renovating my new home. We have painted the entire house and I learned how to install wood floors, tile, and backsplash. I think I've found a new hobby! But I will tell you, I'm exhausted and so sore I can barely move...which I think means I am extremely out of shape haha! 

I know how hard this quarantine can be for our mental health so if you need a new buddy, I'm available to chat and help in any way I can. You can find me [here](https://twitter.com/nicalopezdev) on Twitter. I just moved to Denver and would be thrilled to make new friends.

Anyways, lets talk code! In my two previous posts, we've discussed Object Oriented Ruby. You can read part 1 [here](https://nicaa0695.github.io/object_oriented_ruby) and part 2 [here](https://nicaa0695.github.io/object_orientation_pt_2). We talked about the `initialize` method, `setter`'s and `getter`'s and `attr accessor`. Today I want to dive into instance variables. We will start by jumping back into our cat class. We want the cat's to be given a name right when they are *born*. If I  had a cat class that looked like this: 
```
class Cat 
   attr_reader :name
	 def initialize
	    puts 'A new kitten was just born!'
	 end
end
```
If were to jump into irb and type `monty = Cat.new("Monty")` I would get an error: `ArgumentError: wrong number of arguments (1 for 0)`. That is because there is only an `attr_reader` method and we need to add an argument to our initialize method and then say @name = name because we are in an instance method so we have access to [instance variables](http://ruby-for-beginners.rubymonstas.org/writing_classes/instance_variables.html): 
```
def initialize(name)
   puts 'A new kitten was just born!'
   @name = name
end 
```
Now, if we say `monty = Cat.new("Monty")`, we will get back: `A new kitten was just born! #<Cat: 0x00746c7b193ae0 @name="Monty">` and we can call `monty.name` and get back: `"Monty"` which is exactly what we want!

We can go on to do more fun things like giving a cat an age by adding an instance method `@born_on` to our initialize method and adding an `age` method: 
```
def intialize(name)
   puts 'A new kitten was just born!'
	 @name = name
	 @born_on = Time.now
end
def age
   Time.now - @born on
end 
```

Now if we make a new cat with `timothy = Cat.new("Timothy")`, we will get back: 

`A new kitten was just born! #<Cat: 0x0846c7ta79bb9 @name="Timothy", @born_on=2020-04-16 05:02:54>`

Then we can check how old Timothy is at any given time by saying `timothy.age` and we will get back something like `12.066818` saying he's 12 seconds old or `120.848104` 120 seconds old!

Next week I will most likely jump into another OOP topic. Code code code! 

Peace,

Nica

