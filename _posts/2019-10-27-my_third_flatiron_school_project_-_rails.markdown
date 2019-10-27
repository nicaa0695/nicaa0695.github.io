---
layout: post
title:      "My third Flatiron School project - Rails"
date:       2019-10-27 20:27:47 +0000
permalink:  my_third_flatiron_school_project_-_rails
---


I thought, “Oh no, the time has come again, another project?”. I started thinking about what kind of app I wanted to build. I’ve been cooking a lot so I thought maybe I’d add onto/convert my Recipes app. Then I thought it might be more advantageous for me to build a completely new project; I’d learn more. So I decided to build an app that allows you to track your workouts. You can let the app know what you focused on as well as what exercises you did while working out. You can login in with an email and password or login via facebook.

As intimidating it is, I dove right in. Of course I ran into some issues, we all do. Debugging is a pain but at least we learn from our mistakes. I had issues with OAuth, so many, in fact, that I decided half way through the week that it would just be best to start over on this project… So I did. The second time around, I got to re-use some code but just made sure I was more careful about setting up OAuth and I finally figured out what was wrong - In config/initializers/devise.rb under the Oauth section, I had: 

config.omniauth :facebook, ENV['FACEBOOK_KEY'], ENV['FACEBOOK_SECRET']

But I forgot to add the callback URL (callback_url: "http://localhost:3000/users/auth/facebook/callback"). So when I would click "Login with Facebook", it would take me to a page that said "App ID does not look like a valid App ID". Do not make the same mistake I did because trust me, it will drive you crazy! I also added a feature that allows you to filter through the workouts based on what you focused on, for example, arms, legs, back etc. I realized this time around that I really need to start working on being able to talk about my code because I will be expected to do a lot of that at future interviews.

I’m still not the best at CSS because I haven't been focused on styling as much as just learning the rest of the curriculum so for now my app just has a simple background gradient. Prior to the end of the course, I plan on styling all my projects so at future interviews, I have more to “show off”.

I’m looking forward to the Javascript portion of the course. I’ve found a new love for learning to code. I knew coming in that it’d always be harder than I thought, but I’m glad I’m willing to absorb everything and willing to be uncomfortable. Huge shout out to my cohort lead, Morgan VanYperen, for answering any ridiculous questions I have and for always supporting us! On to the next obstacle!
