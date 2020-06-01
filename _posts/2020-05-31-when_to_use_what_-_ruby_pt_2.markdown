---
layout: post
title:      "When To Use What - Ruby pt. 2"
date:       2020-06-01 02:03:02 +0000
permalink:  when_to_use_what_-_ruby_pt_2
---


Hey guys! Hopefully everyone had a nice weekend. I know I did, and now I'm excited to go camping here in Colorado. We get to stay for three nights, I'm looking forward to a few days in nature away from phones, laptops, social media and more bad news. 2020 has been pretty sad... Sometime's you just need to get away. 🌲☀️⛺️🏔 

![](https://lh3.googleusercontent.com/proxy/eh1uPQ4kpL4n1I118apq3iUhC224Y1JXqUobPXX9pCXbC5phzek6TH7P_wPcyoGieiR-W3nhXhiwl8V_AN7I6ytWFm_mixfLCg38a9JgOKjCqp0a4AobA7aRaWQzHtfGyjeYH0GuA1AtRWGituP0ThpCjqPne4Lnf9rnqw)

But, before I go, I wanted to finish up what we started last week. We talked about how for beginners and even for some more expereinced developers, it might be hard to determine when and where to use these Ruby mechanics. We had a list of 9 and we covered 1-4, today I want to cover 5-9. 

**Some key parts in Ruby**

1. Classes
2. Instance Variables
3. Instance Methods
4. Instantiation
5. `attr_accessor`
6. Class Variables
7. Class Constructors
8. Class Methods
9. `self`

**When To Use Them**

Starting where we left off at number 5: 

**`attr_accessor`**, vs. a custom reader/writer, should be used when: 
* You need to provide an interface for reading and writing to instance variable. For example: 
```
class Person
    attr_accessor :name
end
```
However, you should use a custom reader/writer if you want to add more functionality to it. You don't always want your instance variables to be fully accessible from outside of the class. There are plenty of cases where allowing read access to an instance variable makes sense, but writing to it might not (e.g. a model that retrieves data from a read-only source). And then there are cases where you want the opposite.

**Class Variables** should be used: 
*  For properties that belong to the entire class.
*  For instance memoization (rememberig all instances of a class). For example, all the people would be strored in this class variable, `@@all`:
```
class Person 
  @@all = []
	def initialize(name)
	 @name = name
	end
end
```

*  For collaborating data. 

**Class Constructors** should be used:
* To instantiate instances of the class but instead of overriding the initialize method(`Person.new`), we can extend the classes functionality with a custom constructor to create an instance AND save it(`Person.create`):
```
def self.create(name)
   person = self.new(name)
   person.save
	 return person
end
```

**Class Methods**: 
* Operate on the entire class rather than just on an individual instance.
* Can expose the class' scope to the rest of your program.
* Can operate as custom contructors instantiating instances in new and more complex ways.
* Can operate on all their instances via class variables and instance memoization but do not have access to instance scope.
* For example, if we wanted to search for an object, we can encapsulate this logic into a class method, like Person.find_by_name:
```
def self.find_by_name(name)
    self.all.find{|person| person.name == name}
end
```
Now we can find Beyonce just by saying, `Person.find_by_name("Beyonce")`

**`self`**:

* Should be used whenever an object needs to refer to itself in the abstract.
* In an instance method, `self` will always refer to the instance itself.
* In a class method, `self` will always refer to the class itself.
* `self` can be thought of as the thing that wil recieve this method call.

I hope this was helpful. Again, hammering these situations into my head has helped me become a better developer. So thankful to Flatiron School for teaching these things the way they did! 💙

![](https://marcuscript.files.wordpress.com/2017/05/flatironschool.png?w=762)

Peace,

Nica 





