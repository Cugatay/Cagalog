---
title: Building a Web Game - Day Twenty Three
date: '2021-08-04'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

Hello fellows, today is the time. For, finishing this hell messaging. I mean I hope.

After finishing message stuff, we will almost done. Hmm, actually not almost. Because there are still voting to execute, voting to kill, changing avatar, showing avatar in game, fixing victory component's blur, maybe adding game music, designing all avatars, and maybe more. So, I guess we are not even close to finish, huh?

But for god's sake! I gotta finish this game in one month. Yes, that's the plan which is never come true. Soo, let's hit the sack. I mean, let's start.

# After a Small Thinking Process

I'll have to change the whole system about messaging. It was like, you are subscribing to 2 subscription, and they're sending messages if you're authorised. But this is so stupid in every perspective. First, 2 subscriptions for 1 thing is makes no sense, and if you have 2 subscription, it's really hard to handle values. So, I'm gonna use just 1 subscription, and when you send a message, you'll send it with it's chat value (Vampire chat, Villager chat, Dead chat) and you'll receive it if you're authorised. So, that's the plan. But actually I'm nut sure about saving them to database. Because when you die, you'll see the whole dead chat immediately, that would be confusing. So, I may think adding dead chat for later.
