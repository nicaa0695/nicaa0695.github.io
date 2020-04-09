---
layout: post
title:      "Object Oriented Ruby pt. 2"
date:       2020-04-09 02:26:56 +0000
permalink:  object_orientation_pt_2
---


![](https://thumbs.dreamstime.com/b/object-oriented-programming-isolated-icon-simple-element-illustration-technology-concept-icons-editable-logo-sign-symbol-142287627.jpg)

In last weeks blog post, [OOP](https://nicaa0695.github.io/object_oriented_ruby) , I discussed how Object Oriented Programming came to be and talked about the basics. This week I wanted to talk about it a little more because I think it's important to understand and fun to learn. If you've read any of my previous posts, you may know that Ruby is my favorite programming language because you can develop apps quickly with Gems, the syntax is simplistic and readable, and there's usually more than one way to complete any given task so your mind can explore and you don't have to bang your head against the wall trying to figure out the only way to do something. However, no language is perfect, and Ruby has some drawbacks, like it may have a slower runtime speed than some other languages and may have a slower boot-up speed as well. I learned Ruby first and then moved on to JavaScript but Ruby has my heart which may just be because I understand it a little better. 

![](https://res.cloudinary.com/teepublic/image/private/s--INR5N6yS--/t_Preview/b_rgb:000000,c_limit,f_jpg,h_630,q_90,w_630/v1538406427/production/designs/3241084_0.jpg)

Towards the end of Part 1, we went over how to instantiate instances of a class with `new`: `monty = Cat.new`
In our cat class, we can use the `initialize` method (in other languages, this is called a 'constructor') which allows us to create objects with arguments, for example: 
```
class Cat
  def initialize(breed)
    @breed = breed
  end
end
```
Now we can call `new` like this: `monty = Cat.new("Bengal")`
`monty.breed` will give us => `"Bengal"`
The initialize method is called automatically when we use the `new` method. 

Keep in mind that in ruby, all we do is call methods on objects, that's it. It's important to note that "monty" is not actually the cats name (yet!). We need to teach cats how to have names (data). This is where 'setter' and 'getter' come in. 

A setter writes the property of a cat's name: 

```
def name=(the_cats_name)
   @name = the_cats_name
end
``` 
or
```
def eye_color=(color)
   @eye_color = color
end
```
A getter reads the property of a cat's name:
```
def name
   @name
end 
``` 
or
```
def eye_color
  @eye_color
end 
```

So now with these 'setter' and 'getter' methods, we can say: `monty.name = "Monty"`, `monty.eye_color = "Blue"`. Now `monty` will return something like this => `#<Cat:00x043d476e73 @name="Monty", @eye_color="Blue">`

Since writing setter and getter methods can be repetitive and boring, we can use the `attr_accessor` macro instead! So now our cat class is less cluttered and can be easier to write: 
```
class Cat
   attr_accessor :name, :eye_color, :breed, :age
end 
```
The `attr_accessor` macro builds 2 instance methods (reader and writer) to our objects in one line of code rather than six lines! You could use `attr_reader` to add only the reader and `attr_writer`to add only the reader. [Here](https://ruby-doc.org/docs/Einfuhrung_in_Ruby/chp_04/classes.html) is some documention that goes over these macros if you wanted to learn more. In my next post, I'd like to dig even deeper into OO Ruby unless I get a chance to deploy my app, then I will go over that process. Until next time!

Peace,

Nica
