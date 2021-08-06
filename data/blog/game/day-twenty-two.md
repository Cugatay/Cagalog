---
title: Building a Web Game - Day Twenty Two
date: '2021-07-03'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

Finally, I have finally finished the design of Message Modal, and Message Component. And it took more time than it should. It's because I wanted to find the best UI solution for this modal, cuz it's the most important thing in our game. People are gonna talk through of this stuff. So, I had to implement a good user experiment.

And then, after designing this modal, I coded it in a short while. So now, it's ready. But there are three more things. First, I have to change message structure on backend. For now, we are just pushing our messages. It doesn't have any connection with backend, and we are not saving messages. But to send message, we have to update messages. Because we will send every message to users. Not just the sended message. Cuz updating whole messages array is a better solution than sending a single message to clients, it's a bit risky.

After that, I have to implement this messsage subscription to frontend. Otherwise users can't use this of course.

And finally, I will have to add sendMessage function to frontend. And it's looking like the easiest part. But, I may be wrong of course, it wouldn't be for the first time.

So, I'll do these three things. But I will, not now, it's 2pm man! Let me sleep. See ya tomorrow