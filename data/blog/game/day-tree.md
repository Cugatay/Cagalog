---
title: Building a Web Game - Day Three
date: '2021-07-15'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

Hello my friend, again. And welcome to the new Gamelog. I'm gonna call this blog series Gamelog now.

So today's job is too big. Like your mamma, yeah that's not funny anymore. But I was serious about the adjective of job. It's gonna be really tough. Because it's the biggest job of our backend. It's gonna look at the number of users, if it's enough -in this scenario it's 9- game will start. It means we'll start an interval function, which repeats at a certain time interval. And there is a problem. Today I'm really busy, I have a lot of things to do. Like I have an English class, and I have to visit my uncle. They're coming from Germany.

By the way, let me tell you my country a little bit. I live in Turkey, and actually I don't have lots of things to tell, lol. But I can say that Turkish foods are just delicious. And my uncle and his family are coming from Germany, this is kinda regular thing for a lot of family in Turkey. Because in 20 years ago -I guess- a plenty of migration has happened to Germany from Turkey. They lived on a country that they don't know yet. I admire them. That must be a tough job.

So, story time is over. And I remembered that I wrote down some notes about starting game function. Let me copy it here:

> # Starting The Game
> 
> To start the game, the number of users **must** be 9. If it's 9, we'll create a timeout. Because the last user who joined the game have to see the room. 
> 
> And to really start the game, we will give every user a role at the beginning, and will have to create an interval to update the time and inform the users.
> 
> In day time, we'll update user's status to inform users about who is dead. In vote time, we'll let users to use voteToExecute function. In night time, first we will publish who is executed, then will let users to use voteToKill, protectUser and showRole functions. And again, in day time we'll update user's status (or we will use subscriptions to publish who is dead)
> 
> If is there any winner (we'll control this every day and night time) game is gonna end and we'll clear the interval.