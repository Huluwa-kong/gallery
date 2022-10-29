# COM2004/3004 Assignment
## Developing and Evaluating a Word Search Puzzle Solver

```
若您有关于此作业的任何需求，本人主页, 可添加vx：codingtutor 或者qq：122929048
若您有关于此作业的任何需求，本人主页, 可添加vx：codingtutor 或者qq：122929048
若您有关于此作业的任何需求，本人主页, 可添加vx：codingtutor 或者qq：122929048
```
Due: 3:00pm on Tuesday 13th December

Contents
1. Objective
2. Background
3. What you are given
4. How to proceed
5. Additional rules
6. Submission
7. How your work will be assessed
8. Lateness penalty

## 1. Objective
You are asked to build and evaluate a system that can solve Word Search puzzles. The
input to the system will be, i) a set of images of Word Search puzzles photographed
from a puzzle book and stored in png image format, ii) the list of words that are to be
found in each puzzle. The output will be a sequence of word positions indicating the
grid coordinates of the first and last letter of each of the words that are to be found.
Solving the problem will require two stages: building a letter classifier; implementing
a word finding algorithm. Your classifier must operate with feature vectors that
have no more than 20 dimensions. You are given labelled data sets for training and
evaluation, and some template code to help you get started.

## 2. Background

A Word Search is a puzzle game that first appeared in the 1960’s (see Wikipedia) and
which is now commonly found in newspapers and puzzle books. The puzzle consists
of a grid of letters and a list of words that are hidden in the grid. Words appear in the
grid as straight, connected sequences of letters which can run in any direction, i.e.,
including diagonally and backwards. The aim is for the solver to locate each of the
words.
In the lab classes, you have been experimenting with techniques for classification
and dimensionality reduction. In this assignment, you will use the experience you
have gained to build a system for solving Word Search puzzles, i.e., taking images of
word search puzzles and outputting the positions of the hidden words. This involves
taking the image of the full puzzle, cutting it into separate squares (i.e., one square
for each letter) and then classifying the letter images, i.e., as one of the 26 possible
letters, A' to Z’. Finally, you will need an algorithm to search through the grid of
labels to find where the words are hidden. In Word Search puzzles, the words can run
left, right, up, down, or in any diagonal direction. Words can also overlap.
...


