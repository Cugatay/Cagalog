---
title: Building a Web Game - Day Five
date: '2021-07-17'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

So today, I have to make my roadway more explicit. Because I have almost finished half of the backend codes. And today I added protect user function for doctor role. And by the way, I noticed that users and vampires can vote theirselves. I thought that this is a bug for first time. Then I remembered we could vote ourselves in a game. And that was funny, so it is better to keep it.

Our roadway is gonna be like this: We have to implement show role function for seer. That's the easiest part actually. And then, we need to finish the game. If vampires dies, villagers wins. Or if is the count of villagers equal or lower than the count of vampires, then vampires wins

This is an important stuff, but not just this. We don't have any subscriptions and they are more important then I thought. Because my goal is to use them for everything, for reporting who died, who sends message, for saying that the day/vote/night has started, and maybe even for reporting the game has started. So, we'll need to implement subscriptions after the first 2 steps. Then let's continue to work

# At the Midnight

Hello again. I have really good news. The loop has finally finished, and not just it. I fixed some of the bugs for all game functions. And I'm so happy to see that code. And that's it for today, I guess. The next thing that we'll do is subscriptions. Because our game doesn't work without subscriptions. So, see ya tomorrow