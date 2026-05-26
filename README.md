#  Mean and variance of a discrete  distribution


# Aim 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required 

Python and Visual components tool

# Theory

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure 

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


# Experiment 

![image](https://user-images.githubusercontent.com/103921593/229993174-5b67e57e-3e01-4ac4-9f83-410a932b22bf.png)

# Program 

#### DEVELOPED BY : **KABELAN G K**<BR>Reg No : **212224110027**

### Declaring the value of n

```python
import numpy as np
n = int(input("Enter the value of n : "))
print("Value of n =", n)
```

### Getting the inputs

```python
InputVal = {}
for i in range(1, n+1):
    val = int(input(f"Enter the value no {i} : "))
    try:
        InputVal[val] += 1
    except:
        InputVal[val] = 1
print(f"{i} Values Collected Successfully")
```
### Finding Mean

``` python
mean = 0
for key, val in InputVal.items():
    mean += key*(val/n)
print(f"Mean = {mean:.3f}")
```
### Finding Variance

```python 
ex2 = 0
for key, val in InputVal.items():
    ex2 += ((key**2) * val/n)
var = ex2 - mean**2
print(f"Variance : {var:.3f}")
```
### Finding Standard Deviation

```python
from math import sqrt
sdtDeviation = sqrt(var)
print(f"Standard Deviation = {sdtDeviation:.3f}")
```

# Output 

### Refer to the following images to view the output of the program
<img width="490" height="170" alt="image" src="https://github.com/user-attachments/assets/322723e5-1ef3-42a0-bdf7-fbbb697e6148" />
<img width="490" height="256" alt="image" src="https://github.com/user-attachments/assets/2969a7b2-305e-4b0b-b217-7a178f4fe9d1" />
<img width="491" height="175" alt="image" src="https://github.com/user-attachments/assets/2867687c-3cdf-402a-8733-bfc510e8f6c6" />
<img width="490" height="201" alt="image" src="https://github.com/user-attachments/assets/e0193205-2aba-4651-9473-78c3272e495e" />
<img width="490" height="201" alt="image" src="https://github.com/user-attachments/assets/1539d74d-54a3-464c-8e67-7f9b8b8c7bcb" />
<img width="487" height="164" alt="image" src="https://github.com/user-attachments/assets/7f684d8d-a338-4f39-ad9e-897fe8c9d82a" />





# Result 
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

