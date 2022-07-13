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

For example, "void destroyPlayer" means whatever happens when the player dies. If I were to put playDeathEffect(); inside that, it would play the death effect everytime the player crashes. (This may cause the player to never die as you have replaced the function but we will get to that later)

- You don't always <!-- *clips into the Backrooms* -->

- An integer (int), double (double), float (float), and boolean (bool) are different values you can set within the game. An integer is a normal number, a double is a number that can store more digits and values, floats store decimals <!-- doesnt other stuff do that too though? -->, and booleans are a basic true or false value.

For example, "bool hasCheated = true" would tell the game to kick you out of the level because it thinks that just that is happening. The opposite "bool hasCheated = false" would tell the game that you are playing legitimately and it would not try to kick you out of the level.

- A class is a.. uhh with functions (we talked about this earlier) as its members. When you want to change a function, you have to modify the class by using `class $modify(Class Name)`

For example, if I want to make it so that `hasCheated` becomes true when I die/crash, I would modify the PlayLayer by doing `class $modify(PlayLayer) {}` and I would put everything I needed to change in the { } brackets

## An example

Now that we have learned everything, let's actually use this to make a mod.

 - To begin, modify the PlayLayer class

`class $modify(PlayLayer) {}`
 
 - Then, add when you want your code to happen by modifying a function

`class $modify(PlayLayer) {
  void destroyPlayer(PlayerObject*, GameObject*) {}
}

- Finally, you need to add what happens when the player crashes or is supposed to die

`class $modify(PlayLayer) {
  void destroyPlayer(PlayerObject*, GameObject*) {
    playDeathEffect();
  }
}
