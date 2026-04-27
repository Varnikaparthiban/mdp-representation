# MDP REPRESENTATION

## AIM:

The representation of real world scenario using Markov Decision Process (MDP) by stating all the states, actions and environment with respective rewards.

## PROBLEM STATEMENT:

### Problem Description
A Smart Thermostat is an intelligent temperature control system used to maintain a comfortable room environment automatically. It continuously observes the current room condition and decides the best action to perform.

Based on the room temperature, the thermostat can:


Increase Temperature when the room is too cold

Keep Same when the room temperature is comfortable

Decrease Temperature when the room is too hot


The main objective of the thermostat is to keep the room in a comfortable state while avoiding extreme hot or cold conditions.


This real-world scenario can be represented using a Markov Decision Process (MDP), where the next room condition depends on the current state and the action chosen by the thermostat.

### State Space
{0,1,2}

0 = Cold Room

1 = Comfortable Room

2 = Hot Roomm

### Sample State
{0} = Cold Room

### Action Space
{0,1,2}

0 = Increase Temperature

1 = Keep Same

2 = Decrease Temperature

### Sample Action
{0} = Increase Temperature

### Reward Function
+1 : Room becomes Comfortable

0 : No change in room condition

-1 : Room becomes Too Hot or Too Cold

### Graphical Representation
<img width="1663" height="945" alt="image" src="https://github.com/user-attachments/assets/638b4a29-2da4-44ed-882c-27d07d68cad5" />


## PYTHON REPRESENTATION:
```python
P = {
    0: {  
        0: [(0.8, 1, 1, False), (0.2, 2, -1, False)],  
        1: [(1.0, 0, 0, False)],                        
        2: [(1.0, 0, -1, False)]                        
    },

    1: {   
        0: [(0.8, 2, -1, False), (0.2, 0, -1, False)], 
        1: [(1.0, 1, 1, False)],                       
        2: [(0.8, 0, -1, False), (0.2, 2, -1, False)]   
    },

    2: {  
        0: [(1.0, 2, -1, False)],                       
        1: [(1.0, 2, 0, False)],                      
        2: [(0.8, 1, 1, False), (0.2, 0, -1, False)]   
    }
}
```

## OUTPUT:
<img width="555" height="198" alt="image" src="https://github.com/user-attachments/assets/aad02db2-15c5-432d-8823-56d3edb0cf81" />


## RESULT:
Therefore an MDP representation has been created for a real world scenario with all the states, actions and rewards.

