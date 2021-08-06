---
title: Building a Web Game - Day Twenty Three
date: '2021-07-05'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

Yesterday, I had an interesting bug on container of messages. This component is a ScrollView, where you can scroll elements. When new message comes up, it have to scroll down, because otherwise you can't notice that new message has arrived. But it was so interesting, like after two messages, it was scrolling down. And when the game time changes (day, vote, night) it was scrolling again.

Then I tried to understand what is the problem. In coding I always change some part/parts of the solution to understand the problem with this solution. Then I just changed one part and it solved like immediatelly. And it was kind of "Yo, why this is working now, why it didn't take my 5 hours or more?" So long story short, I have messages on client now. And I also implemented send message function to fronted. I mean, now users can send or get messages easily. That's it for today, and we are closer to finish the game now. That's kind of good :D See you.