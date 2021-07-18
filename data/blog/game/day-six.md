---
title: Building a Web Game - Day Six
date: '2021-07-18'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

And here we are, subscriptions! I am scared of subscriptions, because it's really hard to implement for me. But on the other side, I think sockets and subscriptions are the coolest thing that I see, because you can make anything in realtime, and I just love it. Thing that I love in games is multiplayer (I can't play game with my PC, but anyways) and today we'll to this stuff. So guys, wish me luck

# Dear Apollo Server...

Hey Apollo, as you remember, at the one of my blog I criticized something about your new version -v3- I said something bad about you. And I'm not regret at all bro, I don't understand why did you made things so hard? And it's not just me who is saying that. I had to tackle with the changes of this new version again. This time, it was about subscription changes. Now you can't just implement subscriptions easily, really thanks man, it was already hard to do it! Now you have to use some other repos and now you can't use the same context with Queries and Mutations. That sucks.

And it really tired me, so today may be done. But it's so funny to create subscriptions now, because the implementation done now. And also, I have made a checklist again. At the beginning of the day I thought like I don't need to, but then I remembered that "Checklists are good, bro" So here it is:

- [ ]  gamePlayers
- [ ]  gameStarted
- [ ]  gameFinished
- [ ]  gameTimeLog
- [ ]  playerVotedToExecute
- [ ]  playerVotedToKill

They all will be checked, they all...

# I Couldn't Stop

Yeah, as you can guess I have made my first subscription baby! It's gameUpdated. I know that it's not in the checklist, because using this thing is better than using gamePlayers, gameStarted, gameFinished ... At least for now.

Maybe you can tell that splitting functions is a better way than this, but don't forget that I'm developing the MVP version, so this function is more than enough for now, mean don't need to tackle with more subscriptions. And with this function, our checklist will be like this:

- [X]  gameUpdated
- [ ]  playerVotedToExecute (maybe, not sure)
- [ ]  playerVotedToKill
- [ ]  playerSentMessage