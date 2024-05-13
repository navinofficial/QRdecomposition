# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
![image](https://github.com/navinofficial/QRdecomposition/assets/151710204/8764e625-d5c5-4602-b861-008e74f813cc)
## Program:
### Gram-Schmidt Method
# Developed by: Navinkumar v
# Register number: 212223230141
```
import numpy as np
arr=np.array(eval(input()))
n,m=arr.shape
u=np.empty((n,m))
e=np.empty((n,m))
u[:,0]=arr[:,0]
e[:,0]=u[:,0]/np.linalg.norm(u[:,0])
for i in range(n):
    u[:,i]=arr[:,i]
    for j in range(i):
        u[:,i]-=(arr[:,i]@e[:,j])*e[:,j]
        e[:,i]=u[:,i]/np.linalg.norm(u[:,i])
r=np.zeros((n,m))
for i in range(n):
    for j in range(i,m):
        r[i,j]=arr[:,j]@e[:,i]
print(e)
print(r)
```
## Output
```
![image](https://github.com/navinofficial/QRdecomposition/assets/151710204/3d80d570-2ee5-47fb-9be6-bc0eb26328b1)
```
## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
