---
layout: post
title:      "When To Use What - Ruby"
date:       2020-05-28 21:35:54 +0000
permalink:  when_to_use_what_-_ruby
---


Hey guys, I hope everyone's week is going well. Thankfully it's almost the weekend! 🙌 Some interesting things have happened this weekend. One of them being that someone's vehicle in my neighborhood was stolen. The driver drove through a fence and into someones backyard, hitting an electric box and causing a power outage. Here's a picture of it that was posted in the neighborhood Facebook group:

**Can't fix stupid**😅

![](https://scontent.fapa1-2.fna.fbcdn.net/v/t1.0-9/101379560_10158682483099459_2380715653666439168_o.jpg?_nc_cat=102&_nc_sid=b9115d&_nc_ohc=ZMgz-ZLWrM0AX9X9xy4&_nc_ht=scontent.fapa1-2.fna&oh=0bc8b32f02eafc6b51d7524f1f9c2ae2&oe=5EF3C347)

This pissed off a lot of people including myself as it took a few hours out of our work day! If you're going to steal a vehicle, at least make sure you know how to drive. 🤦🏽‍

**Denver Tech Community = Fantastic**

Anyways, this week I've been continuing my AWS course, study study study! I'm loving the material, it's just taking me awhile to get through it. I've also applied for a few jobs and started some pretty good conversations on LinkedIn with some people in the Denver tech community that are willing to answer questions that juniors may have during their job search. Thank you to all that make this community so awesome. I've been invited to virtual meetups, been given insight on what interview processes look like at different companies, and have been building a meaningful network. It's been really cool to connect with people who are passionate about software engineering and about helping others as they were once in the shoes of a code newbie! It's also lead to a couple of intro calls with companies to see if we are a match. I knew moving to Denver would be a fantastic place to be while starting a career in software development. 

![](https://www.womenyoushouldfund.com/wp-content/uploads/2017/01/wysk-socialnetwork1.png)

I'm not sure we will cover all 9 pieces in this weeks blog, let's say we will cover 4 now and 5 next week. For beginners, it might not be clear when to use these mechanics in Ruby. Here are a few situations where you would want to use the following:

**Some key parts in Ruby**
1. Classes
* Instance Variables
* Instance Methods
* Instantiation
* `attr_accessor`
* Class Variables
* Class Constructors
* Class Methods
* `self`

**When To Use Them**

**Classes** should be used when: 

* You need several representaions of the same idea
* When you have data that interconnects. For example, a doctor has many patients. So then it would be safe to say that you have two classes, a doctor class that makes instances of doctors and a patient class that makes instances of patients:

```
      class Doctor
      end

      class Patient
      end
```
* When an object needs a lot of individual tasks
* To organize funtionality together

**Instance Variables** should be used when: 
* You need different instances from the same class to have different values for the same property. 🤯 A simple example might be a people class where each person has a different name: 
```
      class Person
			 def name=(name)
				@name = name
			 end 
			 def name
				@name
			 end
  	end 
		
		eminem = Person.new
		eminem.name = "Eminem"
		
		jessie = Person.new
		jessie.name = "Jessie"
```
Here we see that now each instance of a person can have a different names even though they are instances of the same class. 

**Instance Methods** should be used when: 
* You need to access the internal state of different objects from a different scope.
* When individual objects need functionality, like persisting an instance into a database.
* When you need to manipulate the internal state of an object, like changing a cat's name from GARFIELD to garfield. Here's an instance method that would do that:
```
class Cat 
   def downcase_name!
    @name.downase!
   end
end
```

**Instantiation** should be used when: 
* You want to represent a new individual in your program.
* You have primitive data that you want to reify into a more abstract form.
* You want data to be connected with logic that relates to a concept even if it is global, like a connection to an API.

Really hammering these situations into my mind has helped me become a better and more organized developer. Although it takes time learning when or where to use these things, it's worth it because it will save you time and many, many headaches. I think that's all for today. Like I said, we will cover the remaining 5 in next weeks blog. Have a great weekend everyone!

Peace, 

Nica





