# MDP REPRESENTATION

## AIM:

The representation of real world scenario using Markov Decision Process (MDP) by stating all the states, actions and environment with respective rewards.

## PROBLEM STATEMENT:

### Problem Description
A Smart Thermostat automatically controls room temperature and decides whether to increase temperature, decrease temperature, or keep it same based on the room condition.

### State Space
{0,1,2} = {Cold Room, Comfortable Room, Hot Room}

### Sample State
{0} = {Cold Room}

### Action Space
{0,1,2} = {Increase Temperature, Keep Same, Decrease Temperature}

### Sample Action
{0} = {Increase Temperature}

### Reward Function
+1 If room becomes comfortable
0 If no change
-1 If room becomes too hot or too cold


### Graphical Representation
<img width="1663" height="945" alt="image" src="https://github.com/user-attachments/assets/638b4a29-2da4-44ed-882c-27d07d68cad5" />


## PYTHON REPRESENTATION:
```python
P = {
    0:{   
        0:[(0.8,1,1,False),(0.2,2,-1,False)],   
        1:[(1.0,0,0,False)],                    
        2:[(1.0,0,-1,False)]                   
    },

    1:{  
        0:[(0.8,2,-1,False),(0.2,1,1,False)],  
        1:[(1.0,1,1,False)],                   
        2:[(0.8,0,-1,False),(0.2,1,1,False)]   
    },

    2:{   
        0:[(1.0,2,-1,False)],                 
        1:[(1.0,2,0,False)],                   
        2:[(0.8,1,1,False),(0.2,0,-1,False)]   
    }
}
```

## OUTPUT:
<img width="519" height="249" alt="image" src="https://github.com/user-attachments/assets/20ccc03f-4cad-472d-a98a-73620130c5bc" />


## RESULT:
Therefore an MDP representation has been created for a real world scenario with all the states, actions and rewards.

