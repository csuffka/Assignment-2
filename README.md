#This code calculates the speed a-as seen from Earth, and b-perceived by a passenger on the ship, from user-inputted distances and speeds.

tpass=float(0)  #time percieved by a passenger
tearth=float(0)  #time observed from Earth
c=3*10**8


x=float(input('Enter the distance between the space ship and its destination: '))
v=float(input('Enter the speed the space ship is traveling as a fraction of the speed of light: '))

d=x*(9.4605284*10**15)   #converts light years to meters

gamma=1/(1-(v**2))**(1/2.0)

tpass=d/(v*c)
tearth=tpass/gamma

tpass=tpass/31536000       #converts time from seconds to years 
tearth=tearth/31536000     #converts time from seconds to years

print 'a) The time observed from Earth is: ',tearth, 'years'
print 'b) The time percieved abord the ship is: ',tpass, 'years'
