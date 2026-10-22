# CS 370 – Pirate Intelligent Agent

## Project Overview

I worked on a pirate treasure hunt game where an intelligent agent has to learn how to move through a maze and find the treasure. Instead of giving the pirate a set route to follow, the goal was to train it to make decisions based on what happened during previous attempts. This was my chance to work with deep Q-learning and see how reinforcement learning actually behaves when I run it, rather than just reading about it.

## What I Worked On

I was given starter code that included the maze environment, the TreasureMaze and GameExperience classes, and helper functions for displaying the maze, building the neural network, and testing the pirate. The main part I worked on was the qtrain() function. I filled in the training loop so the pirate could start from different open spaces, choose valid moves, receive rewards, and save its experiences for later training. I also worked with the exploration rate and a target network that updates periodically to help guide training.

One thing that caught me off guard was how much the results could change while the notebook was running. I would see the win rate reach 1.000 and then watch it drop again. At first, I thought something had gone wrong, but the pirate was still exploring and being tested from different starting points. I spent time going back through the training logic, checking the conditions that end a game, and making sure the agent was learning from the moves it made. In the saved run of my notebook, the training eventually reached a 1.000 win rate and passed the completion check at epoch 332. Getting there took more trial and error than I expected.

## What This Taught Me About Computer Science

I think computer scientists do more than write code that produces an answer. A big part of the job is figuring out why a program behaves the way it does, especially when the results aren't what you expected. This project made that pretty clear. The code could run without throwing an error and still leave me questioning whether the pirate was actually learning. I had to pay attention to the results instead of assuming that a working program was automatically a correct one.

My approach to a problem is to break it into smaller pieces and check what each part is doing. With this project, that meant looking at how the pirate selected moves, how the rewards were stored, and when the model was updated. I also learned not to change several things at once if I want to understand what fixed a problem. That is something I can carry into other programming projects and into the data work I do outside of school.

## Responsibility to Users and Organizations

The ethical side of this project might not be obvious because it is just a pirate moving around a maze. But the same idea of learning from past data is used in systems that make decisions affecting real people. If I build something like that, I have a responsibility to test it carefully and be clear about what it can and cannot do. A high score during training does not mean a system will work perfectly in every situation.

I also have a responsibility to the organization using the software. That includes protecting the information it relies on, checking for misleading results, and not presenting a model as more reliable than the testing supports. Working in healthcare data has made me especially aware that a mistake in a system can matter to somebody on the other end of it. For me, responsible development means being willing to question the output, even when the program appears to be working.

## Project File

- `Lewis_Stephen_ProjectTwo.ipynb` — Jupyter Notebook containing the pirate intelligent agent and its training and testing results.
