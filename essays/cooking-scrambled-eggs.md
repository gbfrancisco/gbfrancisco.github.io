---
layout: essay
type: essay
title: Cooking Scrambled Eggs
# All dates must be YYYY-MM-DD format!
date: 2018-11-29
labels:
  - Design Patterns
  - Interview Questions
  - Software Engineering
---

## Cooking that Yummy Scrambled Eggs

<img class="ui medium center image" src="../images/gordoneggs.PNG">

Ever watched that video where Gordon Ramsay demonstrates how to cook the "perfect scrabled eggs"? Did you ever attempt to emulate his recipe only to end up in a kitchen disaster (or *nightmare*)? If you did, then welcome to the failure club, as I managed to taste defeat in my atrocious attempt on a dish that theoretically should be easy to recreate. However, after failing to follow the superstar chef's recipe, that did not deter me from learning how to cook scrambled eggs from other people. One thing I noticed, though, is that most of their scrambled egg recipes have a notable similarity—they all use butter, salt, and pepper!

## Isn't it Obvious to Use Butter, Salt and Pepper?

Of course it is. However, that is not the realization that occurred to me. **You don't need to completely follow all their recipes to end up with a good scrambled egg!** You only needed to use butter, salt, and pepper to make it palatable; the rest is just extra details and flamboyance. Nevertheless, this notion of following the basic recipe, or *pattern* per se, reminds me how computer scientists, particularly software developers, utilize certain recipes to tackle problems related in their field. It allows them to organize their code and have some sort of gameplan or blueprint for work. These ***design patterns*** enable them to surgically idenitify bugs and errors while systematically forming new possible steps that get them closer to a solution for the problem.

## How Do I Cook My Scrambled Egg?

<p align="center">
  <img class="ui medium center image" src="../images/designpattern.PNG">
</p>

I do not have any skills in the art of cooking; even if I follow the basic recipe, I still would inadvertently find ways to fail. I can, however, describe instead the design patterns I have used in my own code. In ICS 211, I picked up a some design patterns. A very notable example would be the factorial problem where we implement a function that gives the factorial of a given input. Obviously at first, I did not have any gameplan as to how to tackle this problem so my inexperienced mind told me to use *for loops*.

```java
public static int forFactorial(int number) {
  if (number == 0) {
    return 1;
  }
  int temp = number;
  for (int i = 1; i <= number - 1; i++) {
    temp = temp * (number - i);
  }
  return temp;
}
```
This was the *scrambled eggs* that resulted from not following any recipe. By the looks of it, the code functions fine, but the *for loop* could possibly perplex novice people who analyze this code. As I learned about recursion, I implemented it into my recipe:

```java
public static int recFactorial(int number) {
  if (number == 0) {
    return 1;
  } else {
    return number * recFactorial(number - 1);
  }
}
```
This code is much neater compared to the former function as it only uses one if else statement rather than incorporating loops in it. In fact, if the person analyzing this code learns about recursion, then this code should be fairly easy to understand. You do not even have to be the Gordon Ramsay of programming to appreciate this *scrambled egg*.

Right now, as an ICS 314 student, we are working with a new type of scrambled egg—one where the egg's structure is divided into different *directories*. Here is one example of an important snippet of the directories:

(Taken from [meteor-application-template-react](https://ics-software-engineering.github.io/meteor-application-template-react/) GitHub page)
```
ui/
  components/  # Contains page elements, some of which could appear on multiple pages. 
  layouts/     # Contains top-level layout (<App> component).
  pages/       # Contains components for each page. 
```
In developing a web application, this strategy breaks down the whole project into small relative pieces that allow the developer to focus on different specific tasks. For instance, in the components directory, the developer could implement a navigation bar (or navbar for short), and because the navbar is treated as a separate component, it can be used over and over again for other parts in the project; the navbar could appear on every single page on the web app. Now, imagine if one tries to develop a web app from scratch without using any sort of template or guidelines. Without a doubt, it is possible but such disregard to a more systematic approach such as design patterns would inevitably result into hard-to-find errors and inefficient, chaotic code.

## In retrospect...

My ICS 111 projects would have been so much better to look at, had I learned about proper design patterns. In fact, I could have finished them efficiently in a timely manner. But alas, that was in the past where I was a just a fledging trying to learn the ropes. Now that I have gained a lot of experience to proceed to a higher level of understanding in this field of Computer Science, it is imperative at this stage to incorporate systematic ways to solve the various problems that arise in this discipline. In other words, rather than aimlessly attacking the problem, one should follow the recipe to make that fluffy, yummy scrambled eggs.

<p align="center">
  <img class="ui medium center image" src="../images/fluffyeggs.PNG">
</p>
