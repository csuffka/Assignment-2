#Assignment 2 Problem 2
#This code takes inputted values of A and Z and prints out the binding energy for the corresponding atom and the binding energy per nucleon.

#imports

a1=float(15.67)              #All a+# variables are in units MeV
a2=float(17.23)
a3=float(0.75)
a4=float(93.2)
a5=float(0)
B=float(0)                  #binding energy
BA=float(0)                 #binding energy per nucleon

A=float(input('Enter the atomic mass number A: '))
Z=float(input('Enter the atomic number Z: '))



if A%2==1:               #Assigns the 5th constant a value dependant on A and Z
    a5=0.0
if A%2==0:
    if Z%2==0:
        a5=12.0
    if Z%2==1:
        a5=-12.0

B=((a1)*A)-((a2)*A**(2/3.0))-((a3)*(Z**2/A**(1/3.0)))-((a4)*((A-2*Z)**2)/A)-((a5)/A**(1/2.0))
print 'a) The binding energy of this atom is: ',B

BA=B/A
print 'b) The binding energy per nucleon is: ',BA
