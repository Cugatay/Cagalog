---
title: Building a Web Game - Day Two
date: '2021-07-14'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

Hello traveller, and welcome to the day two. Today's job is most about building the backend (I guess). But first, I didn't finish the last design page, which is role choice screen. So, I think I should finish it first. And let me show you other designs that I didn't show you yet:

Main Menu:

![Main Screen](https://www.cagataykaydir.com/static/images/gameMainScreen.png)

Avatar Choice Screen:

![Welcome Screen](https://www.cagataykaydir.com/static/images/gameAvatarSelectScreen.png)

So that's it, now we can continue with today's tasks.

# I'm Done With The Design (I Hope)

Now, the screen designes have finished. And I'm sure that it's not finished at all, I'll have to change something in design. But the bad thing about the designs is animations are not explicit. I'll have to find how can I animate things in coding section. That's faster and I think I can handle with this issue. So now, I am able to go with the coding section. Yey, or f•ck.

# Coding Babe

Let's talk about my approach to developing an app. First thing I do is a feature list and page/screen designs. It makes me feel more comfortable, because if I have a design, I also have a guarantie that my app is gonna look like that. And designs also makes frontend coding section easier. Because thanks to designs, you know all components' position and pagination with each other. And now we have finished that section. Now it's time to coding, and let me tell you my coding approach.

# A Little Break

So, I'm here again :D I had a math lesson man, that's tough. Now I'm here. And yeah, let's continue to talk. Finding a coding approach took some of my time. But at the end, the important thing is coding like building a tower. You'll need to build foundations to don't get stuck later. Just like in coding. You need to start from beginning. If you have a design, it doesn't mean that you can start with frontend. Because frontend gets data from backend. So, my plan of building app is now like this:

- Create a Feature List / UI Design (You can split this into two different step of course)
- Create a Back-End Structure (Like database structure and backend function list)
- Code Backend With Looking This Structure And Your Feature List
- Code Frontend With UI Designs
- Connect Backend From Frontend

And I'm also gonna split Subscriptions part (Websockets) as a different step. Because it's gonna be necessary. So, let's start with writing down Backend Structure.

# Writing Backend Structure

Now I think I'm done with writing database structure, and of course here is the notes:

> ## Backend Notes
> 
> - We can note down the time that the game is started. And then, just create a function  that calculates that is the time day,vote or night with elapsed time. Yeah that makes more sense than using an interval function
> - No, we can't. We'll need to inform people. And using intervals is a better solution :(

> ## Database Structure
> - User
>     - _id (MongoDB automatically stores): id
>     - username: string
>     - email: string
>     - password (hash): string
>     - avatar: string
>     - winCount: int
> - Game
>     - players: playerArray
>     - winner: string (winner group name, like villagers or vampires)
>     - startedAt: date
> 
> ## Backend Functions
> - login
> - register
> - changeAvatar
> - joinGame
> - sendMessage
> - voteToKill
> - voteToExecute
> - showRole
> - protectUser

And even though I feel like I haven't worked, I need to rest.

# A Little Supplication

I wanna say something to you, yes you Apollo Graphql. Are you an idiot? Why did you guys just changed the default playground, what were you thinking guys!!!

Just wanted to say this.

# More Supplication

Bro, this so stupid but these days everyone is updating their codes, and they have made their codes so useless. tsconfig.json (I follow the owner btw, he is Ben Awad) and whole Apollo Graphql's playground has changed and this was so hard to use them in my project. This has a really bad feeling, because you feel like doing nothing.

And good news, I finally started to write the important codes. You can see the ![Github Repository](https://github.com/Cugatay/wofgang) to follow all changes. With the written code, I have finished 3 backend function, here is the tasklist:

- [x]  login
- [x]  register
- [x]  changeAvatar
- [ ]  joinGame
- [ ]  sendMessage
- [ ]  voteToKill
- [ ]  voteToExecute
- [ ]  showRole
- [ ]  protectUser

And it's time to start the game, with joinGame function. But it's too late now, the time is 02:13 a.m. now. And I know, today's date is not same with the title now, you are right, I have to continue with new blog. So see ya!