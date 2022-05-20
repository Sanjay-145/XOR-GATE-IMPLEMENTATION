### EX NO : 08
### DATE  : 13/05/2022
# <p align="center"> XOR GATE IMPLEMENTATION </p>
## Aim:
   To implement multi layer artificial neural network using back propagation algorithm.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## Related Theory Concept:
Implementing logic gates using neural networks help understand the mathematical computation by which a neural network processes its inputs to arrive at a certain output. This neural network will deal with the XOR logic problem. An XOR (exclusive OR gate) is a digital logic gate that gives a true output only when both its inputs differ from each other.
The truth table for an XOR gate is shown below:
![image](https://user-images.githubusercontent.com/75235426/169494875-43717804-5ec8-49ff-84a6-d0316b96a204.png)


## Algorithm
1.Import the necessary libraries
2.Define the training data and target data
3.Add layers to the Model
4.Run the model for 1000 epochs and print the results

## Program:
```
/*
Program to implement XOR Logic Gate.
Developed by   : P.Sanjay
RegisterNumber : 212220230042 
*/
```
```
import numpy as np
from keras.models import Sequential
from keras.layers.core import Dense
training_data = np.array([[0,0],[0,1],[1,0],[1,1]],"float32")
target_data = np.array([[0],[1],[1],[0]],"float32")
model= Sequential()
model.add(Dense(16,input_dim=2,activation='relu'))
model.add(Dense(1,activation='sigmoid'))
model.compile(loss='mean_squared_error',optimizer='adam',metrics=['binary_accuracy'])
model.fit(training_data,target_data,epochs=1000)
scores= model.evaluate(training_data,target_data)
print("\n%s: %.2f%%"% (model.metrics_names[1],scores[1]*100))
print(model.predict(training_data).round())
```

## Output:
![XOR GATE](XXX.png)


## Result:
Thus the python program successully implemented XOR logic gate.
