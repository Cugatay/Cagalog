---
title: Building a Web Game - Day One
date: '2021-07-13'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

# Starting With a Good Strategy

So far so now, a didn't started. I'm trying to find a strategy for every single step of my application. And yes, I can hear you. You're asking what is this game. And again, yes. I'm gonna tell ya.

But first, I'll need to create a design. And I'm implementing mobile-first strategy. Of course in every step. This means that, everytime think mobile design, and mobile compatibility first. For design, if you're finding a solution for small-sized screen, you will find a solution for big-sized screen easily. For coding, if you start to coding the mobile design, you'll also need to implement the desktop design. But the difference between starting from desktop and mobile is, mobile devices' RAM is much more worse than desktop devices. So, desktop devices can implement the design changes for big-sized screens easily, they don't affect from the CSS statements. So we will start with mobile. But not in web, in a mobile app.

So, you may say that the title is building a web game. You're right, but I did mean that we're building a Javascript app. Meaning, we'll use React Native first. I'm building a mobile app instead of web, and actually I don't have a mobile experience like I have it at web dev. But I still wanna develop this app on mobile, it has two reasons; one: Everyone is using mobile phones, and two: If I don't have enough experience, it means I will have enough experience

# First Steps and Issues

The app is a **Vampire-Villager game**, or with it's common name: `Werewolf-Villager game`. If you don't know what is that; We have basically two teams: Vampires, and villagers. Vampires tries to kill villagers at midnight, and at sunrise villagers wake up and tries to execute the vampires. Every village people (including vampires) votes someone. And the one who takes more and enough vote dies. In villagers, we have doctor and seer roles. Doctor can protect someone at midnight, from vampires. And seer can check someone's role at midnignt, for sake of villagers. So that's it. `But here is the problem: We need a day-night cycle`, which we don't try with Javascript a lot. And I'll have to find a solution to control this cycle.

# Feature List and Design

Because of my tradition, I have to create a design for my app. That makes easier to implement a style and helps my app to have a better look. And before that, I have to create a feature list, which gains our app an ideology

And I already have a feature list. I wrote down some notes while thinking about the game. So we can skip forward that step. But I really have to make a good design, and I didn't design a UI for a game, and it's looking like it's gonna be tough.

# First Designs

Now, I'm still working on design. Because these days everyone is just looking at the design and deciding that this app is good or bad. And if my target group is my friends, they of course don't know the details of coding or designing any code structure. So they will just be able to look at the design, and this is not their bad beacause as I told you, they can't just understand the code. And now, I have the really basics of the design. And here it is:

![Design basics](https://www.cagataykaydir.com/static/images/gameFirstDesign.png)

And actually, I have made a better job than I thought for first design. Yeah, especially the top side is looking pretty sick man. Love it.

Anyways, now I have to continue with that. The rest of the style will be about every single fine detail. Meaning it will be really boring. But let's get into it.

## Day, Vote and Night Screen
The background colors of day, vote and night section will be different. For now, I have them all, but vote section's color may be changed

![Day Background](https://www.cagataykaydir.com/static/images/gameFirstDesign.png)
![Design basics](https://www.cagataykaydir.com/static/images/gameFirstDesignVote.png)
![Design basics](https://www.cagataykaydir.com/static/images/gameFirstDesignNight.png)