#!/usr/bin/python
class Father():
    def gardening(self):
        print("I enjoy gardening")

class Mother():
    def cooking(self):
        print("I love cooking")

class Child(Father,Mother):
    def sports(self):
        print("I enjoy sports")      

c = Child()     # Calling Child class
c.gardening()   # Calling the method from Father class
c.cooking()     # Calling the method from Mother class
c.sports()      # Calling the method from Child class

print ("**********************************")
print (" ")
print ("**********************************")

class Father():
    def skills(self):
        print("Listening music,writing code")

class Mother():
    def skills(self):
        print("cooking,art")

class Child(Father,Mother):
    def skills(self):
        Father.skills(self)
        Mother.skills(self)
        print("Sports")

c = Child()  # Calling Child class
c.skills()   # Calling the skills method
