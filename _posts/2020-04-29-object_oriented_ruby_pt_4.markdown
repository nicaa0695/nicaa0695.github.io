---
layout: post
title:      "Object Oriented Ruby pt. 4"
date:       2020-04-29 17:14:55 -0400
permalink:  object_oriented_ruby_pt_4
---

![](https://cdn.iconscout.com/icon/free/png-256/ruby-45-1175100.png)

Happy Wednesday everyone! Whew, these past couple of weeks have been intense. We're sort of in a pickle as far as the new house goes. We are living in it but can't unpack alot of things until the baseboards are put in. I am doing some things around the house myself. For other things, I've needed contractors which is rough because I leave the house while they work, which is usually several hours at a time, then come back and disinfect just to be safe. We had a large list of renovations and they're almost complete, thank goodness. I just want to get settled in so I can work from home more comfortably! 

![](https://media1.tenor.com/images/c8adb965ede4d79571a565fd75d454c0/tenor.gif?itemid=5655336)

Other than the renovations, I've been working on the AWS Certified Developer - Associate Certification. I completed the Intro to AWS which was really helpful for learning the basics of AWS and it covered the fundamentals of cloud computing. I'm really enjoying it so far but I will say it's taking a lot of studying! 

Today, I wanted to make a part 4 of Object Oriented Ruby because I've had some really positive reactions to the first three which you can find here: [1](https://nicaa0695.github.io/object_oriented_ruby), [2](https://nicaa0695.github.io/object_orientation_pt_2), and [3](https://nicaa0695.github.io/object_oriented_ruby_pt_3). I'm excited that more people are starting to read my blog! 

![](https://i.pinimg.com/474x/fe/ef/b9/feefb9c637c38ba4f28338b68e484b13.jpg)

**Class Methods and Class Variables**

In parts 1, 2, and 3 we went over how OOP came to be, the things Adele Goldberg and Alan Kay invented, classes, methods, attr_accessors, instantiating instances and more. So let's jump into this further. We know about classes: 
```
class Cat
end
```
We know about instances of a class: 

`Cat.new` => `#<Cat: 0x0846c7ta79bb9 @name="Timothy"`

We know that a method provides functionality to an Object and an instance method provides functionality to one instance of a class. 

When kittens(instances) are born, they don't know how to take care or keep track of themselves. That's the responsibilty of the Cat class. That's where class methods and class variabes come in. Class methods do not operate on an instance of a cat but rather on the cat class in general. They are defined with the self keyword, for example: 
```
def self.all
end
```
And class variables are written with two @ symbols in front, like this: 

`@@all`

To make sure that all the newly born kittens are kept track of, we want them to all be together in an array. We can do that by shovelling(`<<`) them into `@@all`, like this: 

```
class Cat

   @@all = []
	 attr_accessor :name
	 
	 def intialize(name)
	    @name = name
	    @@all << self
	 end
	 
	 def self.all
	    @@all
	 end
end
```

So if we make some new kittens: 
```
lucy = Cat.new("Lucy")
jake = Cat.new("Jake")
nancy = Cat.new("Nancy")
```
We can then call `Cat.all` and we would get back an array of all the kittens: 

`[#<Cat: 0x0074c6a88h012 @name="Lucy">, #<Cat: 0x00746c7b193ae0 @name="Jake">, #<Cat: 0x040fb777g037 @name="Nancy">]`

![](https://s.abcnews.com/images/Lifestyle/HT_best_friends_kittens_1_jt_150526_16x9_992.jpg)

I hope this was helpful to new ruby coders. I'm not sure if next week I will write a part 5 or go over the AWS course. Until then, I'd love to connect on [LinkedIn](https://www.linkedin.com/in/veronicalopezdev/) and [Twitter](https://twitter.com/nicalopezdev).  Two more days until the weekend, happy coding! 

Peace,

Nica






