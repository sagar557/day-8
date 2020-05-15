A. Make a ndarray by using np.arange(120), reshape it into shape of (2,3,4,5) and do the following operation on this new ndarray:
1. Access the value 91 using indexing
2. obtain a range of value 35-39 from this ndarray
3. Make another 1D array from this having values 0 and all multiples of 5
4. obtain mean values on axis-3 elements.
In [ ]:
import numpy as np

b = np.arange(120).reshape(2,3,4,5)

print(a[1,1,2,1],"\n\n")

print(a[0,1,3:],"\n\n")

n= a[a % 5 == 0]
print(n,"\n\n")

print("Mean values of axis-3 elements:")
np.apply_along_axis(np.mean, axis=3, arr=b)
B. Make a numpy ndarray np.linspace(5,20,24), and reshape into shape of (4,6).
1. Split and stack to make array of shape (4,4) such that it contain elements of first, second ,fourth and sixth column.
2. Split and stack to make array of shape (2,2) such that it contain elements of first and fourth row and third and fifth column.
In [ ]:
C = np.linspace(5,20,24).reshape(4,6)
[A0,A1,A2,A3,A4,A5] = np.split(E,[1,2,3,4,5],axis=1)

print("\nStacking of elements of first, second ,fourth and sixth column  to make a array of (4,4) \n",np.hstack((A0,A1,A3,A5)))

[E0,E1,E2,E3] = np.split(E,[1,2,3],axis=0)

[r1,r2,r3,r4] = np.vsplit(e,(1,2,3))

[c1,c2,c3,c4,c5,c6] = np.hsplit(r1,(1,2,3,4,5))

[f1,f2,f3,f4,f5,f6] = np.hsplit(r4,(1,2,3,4,5))

print("\nStacking of elements of first and fourth row and third and fifth column to make a array of (2,2) \n",np.array([c3,c5,d3,d5]).reshape(2,2))
C. Plot a function of log2 and straight line y = 0.5x - 1 using matplotlib and find out approximate value at which they intersect. Make sure you have legend in the figure naming the curve.
In [ ]:
from matplotlib import pyplot as plt

x1 = np.linspace(-20,20)

plt.plot(x1,x1*0.5 - 1,color='red' ,label="y=0.5x+1")

x2 = np.linspace(0.000001,30)

plt.plot(x2,np.log2(x2),color='black' ,label="y=log2(x)")

plt.grid(True)

plt.legend(loc="best")

plt.xlabel("x-label") 

plt.ylabel("y-label") 

plt.show()
