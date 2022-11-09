# CS325: Analysis of Algorithms, Winter 2022
## Group Assignment 3
Due: Tue, 11/15/22

The art exhibition organizers again!! Yes, after the successful exhibitions in Corvallis, they are
trying to organize a tour of shows now. They plan to visit n towns t1; t2; : : : ; tn in this tour. They
want to start the tour from t1 and end it at t1. They have a small problem though. With the
very expensive art pieces in their truck they do not want to stop in between the towns to  ll their
gas tank. In other words, they want to re ll their tanks only when they are in a town. But, they
are  ne taking paths that are not necessarily the shortest. For example, when going from t1 to t2,
they allow themselves to pass through other towns if needed. In order to make this trip possible
they are ready to change the tank of their trunk to have a larger capacity. But, they want to know
the smallest possible capacity with which this trip is possible. They took the time to calculate the
required gas to drive between any pair of towns. Now, they are asking us to design an algorithm
that calculates the minimum required tank capacity to  nish the tour from these numbers.
Formally, they give us the number of towns, n, and the gas they need to drive between any pair
of them, gi;j for all 1   i < j   n whenever there is a direct road between ti and tj . In the output,
they just ask for one number, the minimum capacity of the tank that allows completing the tour.
Consider the examples in the following  gure. The left side one is an example with three towns, in
which the answer is 4; the optimal tour is t1 ! t3 ! t1 ! t2 ! t1. The right side one is an example
with four towns, in which the answer is 4; the optimal tour is t1 ! t2 ! t3 ! t2 ! t4 ! t2 ! t1.

Design an algorithm to compute the minimum required capacity of the tank, for a problem
with n towns and m roads. Any algorithm with polynomial time in n and m receives the
full credit for the report part. For the implementation, we try to build test cases so that any
algorithm with O(mlog n) time (with a reasonable hidden constant factor) can pass them.
• Prove that your algorithm is correct, and analyze its running time.
Report (60%). In your report, include the description of your algorithms, running time analysis,
and proof of correctness. Algorithms should be explained in plain english. You can use pseudocode
if it helps your explanation, but the grader will not try to understand complicated pseudocode.
Code (40%). Submit a python program that computes the minimum required capacity of the
tank. Your program will be tested against several test cases, for correctness and e ciency. For
each test case, the program will be automatically stopped after 30 seconds if it is not done in that
time. In this case, the group will miss the points of that test case.
Note: it is important that your output is formatted as described below, since your codes will
be tested automatically. Speci cally, you must implement the function \minimum tank capacity"
in the following code. The code you submit will be an implementation of this procedure in a  le
named \assignment3.py".


