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

The graph should include:

1. States as nodes.
2. Actions as arrows.
3. Rewards on transitions.
4. Transition probabilities if applicable.


---

## Python Representation


```python
# State Mapping
# 0 = Cold
# 1 = Comfortable
# 2 = Hot

# Action Mapping
# 0 = Increase Temperature
# 1 = Maintain Temperature
# 2 = Decrease Temperature
# MDP Representation using Python
print("Name: PRIYADHARSHINI S")
print("Register Number: 212223240129")

mdp = {
    0: {
        0: [(0.8, 1, 10.0, False),
            (0.2, 0, -5.0, False)],

        1: [(0.7, 0, -5.0, False),
            (0.3, 1, 10.0, False)],

        2: [(0.9, 0, -5.0, False),
            (0.1, 1, 0.0, False)]
    },

    1: {
        0: [(0.8, 1, 5.0, False),
            (0.2, 2, -5.0, False)],

        1: [(0.9, 1, 5.0, False),
            (0.1, 2, -5.0, False)],

        2: [(0.8, 1, 5.0, False),
            (0.2, 0, -5.0, False)]
    },

    2: {
        0: [(0.9, 2, -5.0, False),
            (0.1, 1, 0.0, False)],

        1: [(0.7, 2, -5.0, False),
            (0.3, 1, 5.0, False)],

        2: [(0.8, 1, 10.0, False),
            (0.2, 2, -5.0, False)]
    }
}

print(mdp)

```
---
## Output

<img width="1371" height="153" alt="image" src="https://github.com/user-attachments/assets/628b5115-643a-40a9-bcd8-0de13a3580b9" />

---

## Result

The smart room temperature control problem was successfully represented as a Markov Decision Process. The temperature conditions were represented using numerical states 0, 1, and 2, while the possible thermostat actions were represented using numerical actions 0, 1, and 2. Transition probabilities and rewards were defined to model the changes in room temperature and encourage the thermostat to maintain a comfortable temperature.


---

