# modified_a_star

Many people are aware of the A* algorithm, which is a path-finding algorithm that takes a heuristic approach to finding a path from *Point A* to *Point B*. If you are not familiar, here is an **amazing** [reference](http://theory.stanford.edu/~amitp/GameProgramming/) to learn all about it.

## Basic A* Overview
As a basic overview, A* determines the best path to go from *Point A* to *Point B* through calculating the distance from the *start* and distance from the *destination*. 
The goal is to find the next step that will **maximize the distance from the start** and **minimize the distance from the destination**. 

## Inspiration
Currently, with vehicles, path-finding is done through applications such as Google Maps, Apple Maps, Waze, etc. 
Basically, each vehicle is equipped to help the driver reach their destination based on **current conditions**.

But, what if Google Maps gave 100 different users, all driving to the nearest NFL stadium for a game, the same general route, ie. even if the current conditions on that path are good, how do we account for **future congestion**?

## My Idea
I thought it would be cool if I tried to implement A*, but add an addition calculation in the heuristic that would **account for congestion**.

Suppose there was **Road A**, that 3 vehicles are planning to travel on. 
The **first vehicle** that starts its journey **get's priority** over the other two.
Then the **second vehicle**, when calculating it's route, see a higher congestion value on the roads that **first vehicle** took, and will try to optimize based on that to minimize congestion.
The **third vehicle** will do the same, but take the first two into account instead of just the first one.

I also added a **time constraint** variable to take into to account when the person has to reach a destination by a certain time (as minimizing congestion might increase travel time significantly).

Please visit the webpage to see a demonstration of the algorithm.

Link to Webpage: https://vspenubarthi.github.io/modified_a_star/

Instructions on how to interact with the algorithm as well as this information mentioned above can be found there.