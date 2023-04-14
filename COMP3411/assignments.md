若您有关于此文件夹下任何作业的任何需求，可添加vx：codingtutor 或者qq：122929048


# COMP3411/9814 Artificial Intelligence Term 1, 2023

## Assignment 3 – Planning and Machine Learning
**Due: Week 10 - 10pm Friday 21 April**

Marks: 10% of final assessment for COMP3411/9814 Artificial Intelligence

### Question 1: Planning (4 marks)
Modify the simple planner from the week 7 lecture so that it can solve the planning
problem in the textbook, Poole and Mackworth Section 6.1. Here, there is a robot that
can move around an office building, pickup mail and deliver coffee.
Like the rubbish pickup problem, actions can be representation by a triple:
```commandline
    action(Action, State, NewState)
```
where the state of the world is represented by a quintuple:
```commandline
    state(RLoc, RHC, SWC, MW, RHM)
```
- RLoc - Robot Location,
- RHC - Robot Has Coffee,
- SWC - Sam Wants Coffee,
- MW - Mail Waiting,
- RHM - Robot Has Mail

You are required to replace the action specifications by a new set that specify the state
transitions for each of the actions:

- mc - move clockwise
- mcc - move counterclockwise
- puc - pickup coffee
- dc - deliver coffee
- pum - pickup mail
- dm - deliver mail.

Do not alter the planner code, only the action clauses should be replaced.
You should only need to write one clause for each action, however, you might need
some addition clauses to help with the mc and mcc actions. Think about how to
represent the room layout.


Your program should be able to satisfy queries such as:

```commandline
    ?- id_plan(
        state(lab, false, true, false, false),
        state(_, _, false, _, _),
        Plan).
    Plan = [mc, mc, puc, mc, dc]
```
which asks the robot to get Sam coffee. Note that the values of the state variables, RHC,
SWC, MW, RHM are boolean and we’ve used the constants true and false, to represent
the boolean values. The initial state in this example has the robot in the lab, the robot
does not have any coffee, Sam wants coffee, there is no mail waiting and the robot does
not have any mail. The goal state is where Sam no longer wants coffee. Note that the
anonymous variable, ‘_’, indicates that we don’t care what the other values are.
To test your action specifications, think about how you would ask the robot to pickup
mail. What about if Sam want coffee and there was mail waiting?


### Question 2: Inductive Logic Programming (6 marks)

Duce is a program devised by Muggleton [1] to perform learning on a set of
propositional clauses. The system includes 6 operators that transform pairs of clauses
into a new set of clauses. Your task is to write Prolog programs to implement 3 of the 6
operators. One is given as an example to get you started.

**Your answers should preserve the order of literals in each clause, as given. Any new
literals should be appended to the end of the clause.**

Inter-construction. This transformation takes two rules, with different heads, such as
```commandline
    x <- [b, c, d, e]
    y <- [a, b, d, f]
```
and replaces them with rules
```commandline
    x <- [c, e, z]
    y <- [a, f, z]
    z <- [b, d]
```
i.e. we find the intersection of the bodies of the first two clauses, invent a new predicate
symbol, z, and create the clause z ← [b, d]. Create two new clauses which are the
original clauses rewritten to replace [b, d] by z.
To make processing the rules easier, we represent the body of the clause by a list and we
define the operator <- to mean “implied by” or “if’.

A Prolog program to implement inter-construction is given as an example to give you
hints about how to write the two operators.

...