---
layout: default
title: Starting Out
nav_order: 5
description: "Starting out using Geode"
---


# Starting Out

Want to start coding in Geode but have 0 prior knowledge in coding? This is the section for you!

## Resources

Here are a few resources you could use to get started:

- [Bindings](https://github.com/geode-sdk/sdk/blob/main/bindings/GeometryDash.bro)
- [This Documentation](https://geode-sdk.github.io/docs/)
- [The Geode SDK Discord](https://discord.gg/9e43WMKzhp)

## Understanding the basics

Here are some things you will need to know before starting:

 - A function is the thing you see next to "void" in the Bindings file. This is used to define what happens when the specified event occurs.

For example "void destroyPlayer" means whatever happens when the player dies. If I were to put playDeathEffect(); inside that, it would play the death effect everytime the player crashes. (This may cause the player to never die as you have replaced the function but we will get to that later)

- An integer, double, float, and boolean are different values you can set within the game. An integer is a normal number, a double is a number that can store more digits and values, floats are (honestly IDK how to explain someone help here), and booleans are a basic true or false value.

For example "bool isCheating = true" would tell the game to kick you out of the level because it thinks that just that is happening. The opposite "bool isCheating = false" would tell the game that you are playing legitimately and it would not try to kick you out of the level.
