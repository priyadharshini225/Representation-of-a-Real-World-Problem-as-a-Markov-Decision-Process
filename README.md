# Representation-of-a-Real-World-Problem-as-a-Markov-Decision-Process


## Aim

To represent the real-world problem of smart room temperature control as a Markov Decision Process by defining its states, actions, transition probabilities, rewards, and Python representation.

---

## Problem Statement

### Problem Description

A smart thermostat automatically controls the temperature of a room. It observes the current room temperature and decides whether to increase the temperature, decrease the temperature, or maintain the current temperature.

The objective is to maintain a comfortable temperature while reducing unnecessary energy consumption. This problem can be represented as a Markov Decision Process because the next room temperature depends on the current temperature and the action taken.

---

## MDP Components

A Markov Decision Process is represented as:

$$
MDP = (S, A, P, R, \gamma)
$$

Where:

| Symbol | Meaning |
|---|---|
| $S$ | Set of states |
| $A$ | Set of actions |
| $P$ | Transition probability function |
| $R$ | Reward function |
| $\gamma$ | Discount factor |

---

## State Space

The states represent the current temperature condition of the room.

S={0,1,2}
| State Number | Meaning     |
| ------------ | ----------- |
| **0**        | Cold        |
| **1**        | Comfortable |
| **2**        | Hot         |

---

## Sample State

s= 0

This means the room is Cold.


---

## Action Space

You can also represent actions using numbers:

A={0,1,2}
| Action Number | Action               |
| ------------- | -------------------- |
| **0**         | Increase Temperature |
| **1**         | Maintain Temperature |
| **2**         | Decrease Temperature |


---

## Sample Action

a=0

This means Increase Temperature.

---

## Transition Probability

The transition probability explains how the environment moves from one state to another after an action is taken.

General form:

P(s
′
∣s,a)

This means the probability of reaching the next state s
′
 after taking action a in the current state s.

Example:

P(1∣0,0)=0.8

This means that if the current state is 0 (Cold) and action 0 (Increase Temperature) is taken, there is an 80% probability of moving to state 1 (Comfortable).

---

## Reward Function

The reward function defines the feedback received by the agent after taking an action.

General form:

R(s,a,s
′
)

The rewards are defined as:

+10 → Room reaches a comfortable temperature.
+5 → Room remains comfortable.
−5 → Room remains too cold or too hot.

Examples:

R(0,0,1)=+10

The room changes from Cold (0) to Comfortable (1), so the agent receives a reward of +10.

R(0,0,0)=−5

The room remains cold, so the agent receives a reward of −5.



---

## Graphical Representation

Write your answer here.

Draw the MDP graph.

The graph should include:

1. States as nodes.
2. Actions as arrows.
3. Rewards on transitions.
4. Transition probabilities if applicable.


---

## Python Representation

Write your code here.

Use Python dictionaries to represent the MDP.


```python
# MDP Representation using Python
# print("Name:       ")
# print("Register Number:     ")

```
---
## Output

Write your Python output here.


---

## Result

Write your result here.



---

