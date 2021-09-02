# Assignment
Assignment for a internship

#To Access all modules
from array import *

#initialisation of array
arr= []
#To take input from user
n= int(input("Enter the length of the array"))
#Storing in Array
for i in range(n):
    x=int(input("Enter the value"))
    arr.append(x)

print(arr)
#Creating Function to assign zeroes in front of array 
def zeroes_in_beginning(z):
    length=len(z)
    a=length-1 #for storing array
    b=length-1 #for reading array

    while(b>=0):
        if z[b]!=0:
            z[a]=z[b]#non zeroes value stored at the end of array in order
            a-=1
        b-=1    
    while(a>=0):
         z[a]=0;#assigning 0's for the indexes left in array
         a-=1
         
zeroes_in_beginning(arr)
print("zeroes in front", arr)
