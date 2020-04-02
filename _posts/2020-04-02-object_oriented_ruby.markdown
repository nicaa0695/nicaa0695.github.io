---
layout: post
title:      "Object Oriented Ruby"
date:       2020-04-02 19:30:02 +0000
permalink:  object_oriented_ruby
---


In last weeks blog, I talked about how this weeks post would be about the issue with my login system for my Real Estate app and my process for deploying the app with Heroku. However, I didn't have time to complete my project as planned. We just purhased a new home and we were planning on moving towards the end of April but there were some bumps in the road and now we are having to move sooner which is not ideal considering the pandemic and the stay-at-home orders but we really don't have a choice. We didn't hire any movers because we don't want to risk the spread of COVID-19 so it's more exhausting and taking a little longer than we anticipated. Oh wait, I have an idea: 

![](https://i.pinimg.com/736x/a3/4f/4f/a34f4fec31f3d074146a6bec6c1f89d5.jpg)

Just kidding.

So anyways, I will cover deploying the app with Heroku in one my upcoming blogs. For now, I wanted to talk a little bit about obect orientation (OO) in general and then go into Object Oriented Ruby. When learning to code, I think it's not only important but also interesting to understand how computer programming and OO came to be. I will briefly summarize what I learned about OO at Flatiron and share some resources that you can read to further your understanding. In 1969, the founder of Xerox, Joseph Wilson decided to open up a separate reaserch center in Silicon Valley called Xerox Palo Alto Reasearch Center (XPARC) because there were other huge companies there such as IBM and Intel. He hired Adele Goldberg and Alan Kay and they go on to invent the following: 
* Object Oriented Programming 
* Desktop Computer 
* Laptop Computer
* Tablet Computer
* Windows, Menus, Icons, and Pointers
* The Mouse - the ability to click items on the screen instead of typing everything
* Graphical User Interface (GUI) - instead of just a bunch of numbers
* Graphical Operating Systems
* Model-View-Controller Architecture - which I wrote about [here](https://nicaa0695.github.io/the_mvc_structure_and_my_real_estate_app)
* Smalltalk (A programming language)
* Laser Printer
* Ethernet

[](https://i.imgflip.com/3v4ogg.jpg)

Then, long story short, Steve Jobs came in and basically stole all of these ideas and used them to build the Macintosh and Lisa computers among many other things. You can read more about it [here](https://zurb.com/blog/steve-jobs-and-xerox-the-truth-about-inno) and [here](https://web.stanford.edu/dept/SUL/sites/mac/parc.html). 
So what is OOP? It's a model that helps you design software around data and objects rather than logic and functions. It lets us create new things, whether is be a person, a cat, a car, etc. For example we can create a person [class](https://ruby-doc.org/core-2.5.3/Class.html) that allows us make instances of people and have those people introduce themselves with methods:

```
class Person
   attr_accessor :name, :age
   def introduction
      "Hello, my name is #{self.name} and I am #{self.age} years old!"
   end
end
```

Now we can say: 
```
nica = Person.new
nica.name = "Nica"
nica.age = "24"

nica.introduction
```
Which will output: "Hello, my name is Nica and I am 24 years old!"

The best way to become comfortable is by typing 'irb' into your terminal and creating objects with Interactive Ruby. 
Some things to keep in mind while you're playing around in irb: 
* Class definition - What your class produces, for example:
 ```
 class Cat
 ```
* Class body - What instances of your class can do, for example:
```
def say_hi 
    puts "Meow"
end 
```
* Instantiation - Bringing an object to life, for example: 
```
monty = Cat.new
```
* Object ID - All objects in Ruby have an ID, for example: 
```
monty.object_id
```
would output somethinng like `=> 008647628740` and that is what makes each object different until you teach them all how to do the same things with `initialize` method, which we will get to later! 

For now, have fun, code alot, stay home as much as possible and stay healthy! 

Peace, 

Nica







