---
title: Building a Web Game - Day Seven
date: '2021-07-19'
tags: ['react', 'code', 'game', 'typescript']
draft: false
summary: I'm Trying to Build a Web-Based Game
---

As you can remember, we were about to finish the backend code. And now, we are closer than ever! I have every single subscription but sendMessage. Let me paste the code here:

```javascript
Subscription: {
    // gameUpdated subscription:
    gameUpdated: {
        subscribe: withFilter(() => pubsub.asyncIterator('GAME_UPDATED'), async (payload, variables) => {
        const user = await verifyUser(variables.token);

        const game = await SubGameModel.findOne({
            players: { $elemMatch: { username: user.username, isAlive: true } },
            winner: null,
        });

        return payload.gameUpdated._id.toString() === game?._id.toString();
        }),
    },
    // gameUpdated subscription:
    playerVotedToExecute: {
        subscribe: withFilter(() => pubsub.asyncIterator('PLAYER_VOTED_TO_EXECUTE'), async (payload, variables) => {
        const user = await verifyUser(variables.token);

        const game = await SubGameModel.findOne({
            players: { $elemMatch: { username: user.username, isAlive: true } },
            winner: null,
        });

        return payload.playerVotedToExecute.game_id.toString() === game?._id.toString()
        && payload.playerVotedToExecute.player_username !== user.username;
        }),
    },
    // playerVotedToKill subscription:
    playerVotedToKill: {
        subscribe: withFilter(() => pubsub.asyncIterator('PLAYER_VOTED_TO_KILL'), async (payload, variables) => {
        const user = await verifyUser(variables.token);

        const game = await SubGameModel.findOne({
            players: { $elemMatch: { username: user.username, isAlive: true } },
            winner: null,
        });

        const player = game?.players.find((pl) => pl.username === user.username && pl.role === 'vampire');

        return !!player && payload.playerVotedToKill.game_id.toString() === game?._id.toString()
        && payload.playerVotedToKill.player_username !== user.username;
        }),
    },
},
```

So, for sending message, we have a different structure about it. Because we are not gonna save any message on database. Instead, we will just send the message with subscriptions. And to send message, we need to create a mutation. You may thinking like, why do we need to create a mutation, we just need a subcription. Yes my friend, we need a subscription, but to use subscription, you always need Mutation/Query function. That's actually pretty good, because you can do something on mutation and then publish things with subscription in this scenario. So I love this feature. Graphql <3

Before we start to create this mutation, I have to tell you something. I missed a point on game players. We need to show their avatars. And this is not hard, but the thing, I am not sure about how I want avatars in game. Because I want the avatars customisable. Like you can select your eye color, your hat etc. But I'm not an illustrator. So I'll need to find a stock image, but I don't want this. Because I'll never be sure about copyrights if I use stock. Instead, I want one of my friend to work on this images, beacuse I think he's really good at this, and I want him to have a project, because that's cool. These are the personal reasons. But if you want non-personals, special images makes this project more special I guess. So I'm gonna talk to him when I'll close enough to finish this project. Or maybe I will talk to him 1 hour later, I'm untrustable as you don't know.