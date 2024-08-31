# Assignment 26

# Assignment part 1: Gridworld
## Objective:
To understand Q learning and explain with pseudo code on the working.

## Psuedo Code 

- __init__
    - creates grid template with reward and noise(moving in unintended direction probability) as parameters

- getQValue
    - based on state and action, it returns q value

- computeValueFromQValue
    - This returns state when action is max, considering all possible actions

- computeActionFromQValues
    - This returns an action which gives maximum q values for given state
                    
- getAction
    - returns policy at the state( no exploration happens)

- update
    - This function updates the q values based on state, action, nextState, reward

## Pre requisites:
    python 2.7

## Execution command
Create a python 2.7 virtual environment. Run,
    python Gridworld.py -k 100 -a q -s 10000

## Results
![img](grid.png)

# Car Simulation 
        
## Pre requisites:
- Env : python 3.6.9 and can run till python 3.9
- pip install kivy

## Environment Creation and running program:
- From google map I have taken the are where I live.
- Cropped the image from the satellite map by  making labels off.
- Using Libre Offie Draw(Ubuntu) oe MS Paint(windows), all navigation path are created.
- This includes drawing path for main roads and sub roads etc. 
- The main image is removed and drawn image is saved as MASK.png
- The same image is 90 degree rotated and and saved as MASK1.png.
- The program is run from command line using :
  python map.py
- sand.jpeg is created/updated as program learns during training

## Demo    
[![Watch the video](https://img.youtube.com/vi/R9vKHr1zBeI/0.jpg)](https://youtu.be/R9vKHr1zBeI)
    
## Questions

Q1. What happens when "boundary-signal" is weak when compared to the last reward?

Answer: When the "boundary-signal" is weak relative to the last reward, the car tends to stuck at the boundary. It struggles to return to the road or to reach its goal set.

Q2. What happens when Temperature is reduced?

Answer: The car movement was fluctuating very rapidly in sthe stimulation. The temperature controls the "exploration-exploitation trade-off". With lower temperature can led to reduced exploration and increased exploitation.

Q3. What is the effect of reducing gamma? 

Answer: By reducing the gamma value  can have averse results in overall result. The agent may not focus to reach the goal but be happy in staying on roads by getting current rewards.

