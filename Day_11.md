Geometric Distribution

Type: Discrete probability distribution
Used to model number of trials till we get the first success
Example: Toss a coin and find the number of tosses till we get the first head
P(Success) = p = 0.5
P(Failure) = q = 0.5
Number of trials to reach first success = X
PMF: P(X = k) = (1 - p)k - 1  p
Example, probability of getting the first head on the third trial = PMF (X = 3) = (0.5)3 - 1  0.5 = (0.5)2  0.5 = 0.25 x 0.5 = 0.125
Expected number of trials to get the first success = E(X) = 1/p

---

What is Linear Programming Problem (LPP)?

Linear Programming Problem (LPP): Mathematical method to find the best possible outcome (e.g. maximize profit/minimize loss) in a situation where we have limited resources
Key concepts: Objective function and Constraints
Objective function: Our goal, e.g. Maximize: Profit = 5x + 3y, where x and y are quantities that we can control
Constraints: Limitations, e.g. limited raw material, time, money, e.g. x + y <= 100

---

LPP Example

Problem
We run a factory making chairs (Rs 300 profit per chair sold) and tables (Rs 1,000 profit per table sold) 
We 400 units of wood: One chair needs 5 units, one table needs 10 units
We have 300 hours of worker time: One chair takes 2 hours, one table needs 6 hours
How many tables and chairs should we make to maximize profit?
Steps
Objective function: Maximize 300x + 1000y (profit)
Constraints
5x + 10y <= 400
2x + 6y <= 300
x, y >= 0 (Non-negative quantities)
LPP_chairs_tables.py

---

Car Example

A car manufacturer manufactures two cars A and B
There are one robot, two engineers, and one detailer at work
The detailer is going on a short holiday, so he only has 21 working days available
The two cars need the following resource times
Robot time: Car A – 3 days; Car B – 4 days
Engineer time: Car A – 5 days; Car B – 6 days
Detailer time: Car A – 1.5 days; Car B – 3 days
Car A provides €30,000 profit, whilst Car B offers €45,000 profit
Optimize the car production

Decision variables
x = Number of A cars to be produced
y = Number of B cars to be produced
Objective function
Maximize Z = 30000x + 45000y
Constraints
Robot time (R): 3x + 4y <= R
Engineer time (E): 5x + 6y <= 2E
Detailer time (T): 1.5x + 3y <= 21
Non-negativity: x >= 0, y >=0 
Problem
Find Maximum Z

---

Summary

Objective function
Maximise Profit = 30,000 x A + 45,000 x B
Constraints
A≥0
B≥0
3A+4B≤30
5A+6B≤60    ... Note that we have 2 engineers, so this is not 30; but it is 60
1.5A+3B≤21

---
