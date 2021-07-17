---
title: Building a Web Game - Day Four
date: '2021-07-16'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

I couldn't work on this project like other days in yesterday. But I coded joinGame function. The thing I have to code is the game loop. So, it's what I'm gonna do today. But before we start, I'm gonna share the start the game function code. It would help you to understand:

```javascript
// helpers/startGame.ts ->

import { IGame } from '../models/GameModel';
import { Document } from 'mongoose';

const startGame = (game: IGame & Document<any, any, IGame>) => {
  const { players } = game;

  const roles = ['seer', 'doctor', 'vampire', 'vampire', 'villager', 'villager', 'villager', 'villager', 'villager'];

  // The Fisher-Yates Algorithm ->
  const shuffleArray = <T>(array: Array<T>) => {
    for (let i = array.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      const temp = array[i];
      array[i] = array[j];
      array[j] = temp;
    }
  };

  shuffleArray(roles);

  for (let i = 0; players[i] !== undefined; i++) {
    const player = players[i];
    player.role = roles[i];
  }

  game.save();
};

export default startGame;
```

# The Most Important Part: Game Loop

I said myself that It's time to get through of this. And started to write the code. Then I noticed that it's bigger than I thought. Because, everything is gonna be in this loop, like finishing the game, calculating votes and protecting something.

So, to splitting the code, I didn't write everything in loop. Instead, I created day, vote, and night functions. So now, that's easier to control them. And that's it for today. Actually the bad thing about backend coding is this. You can write a lot of code, but it makes one job, and there is nothing to show. In designing section you have your designs to show; in frontend, you have your screens. But in backend that's it :D