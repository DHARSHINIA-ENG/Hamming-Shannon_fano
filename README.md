# Huffman-Shannon_fano
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
## Aim:
To apply the Huffman and Shannon-Fano source with symbols and statistics {0.125,
0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output.

## Tools Required:
Python IDE with Numpy and Scipy

## Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```


## Calculation:

![WhatsApp Image 2025-03-29 at 09 33 51_787a13c0](https://github.com/user-attachments/assets/042729a0-9f3b-4ffd-ac75-2d45021c9d2f)
![WhatsApp Image 2025-03-29 at 20 12 01_8587786e](https://github.com/user-attachments/assets/f1c9a867-c8ef-4089-b0ff-f3134ecc4cfc)

![WhatsApp Image 2025-03-29 at 09 33 51_f4361652](https://github.com/user-attachments/assets/8df631eb-32d9-480f-b9df-fb5f1b8024f4)


## Output:
![Screenshot 2025-03-29 090149](https://github.com/user-attachments/assets/dda112c8-8316-4bea-9a56-aa58ba5dfd70)


## Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625,
0.125, 0.125, 0.25} using python are verified
