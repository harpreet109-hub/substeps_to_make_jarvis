procedural - just writing the code line after line to be ran in an order.
functions- improved re usability 
OOPS - decrease redundancy and increase re usability  
in oops first class is made and then objects are added to it, class in a blueprint for creating object 
--> code snippet:-                                                                                                             output :- harpreet singh
      #creating class:- 
      class Student:              #class's name is generally started with a capital letter
          name="harpreet singh"
      #creating object:-
      s1=Student()  
      print(s1.name)



*******__init__ -> executed during object creation*******
all classes have a function called __init__() function that is executed when the object is being intitated

code :- 
_**      #creating class:- 
class Student:              #class's name is generally started with a capital letter
    name="harpreet singh"
    # constructor ->init
    def  __init__(self , ):
        print(self)
        print("hello")


#creating object:-
s1=Student()
print(s1.name) **_

init takes to arguments :- first one is self -> self is just a reference to current object.
                           second one is a variable , that can be assigned any value while creating object.

_**#creating class:- 
class Student:              #class's name is generally started with a capital letter
    name="harpreet singh"
    # constructor ->init
    def  __init__(self , fullname):
        self.name=fullname;
        print("hello")
#creating object:-
s1= Student("karan");       # creates object named karan and assigns value to variable( second argument of init)
print(s1.name)**_


the constructor with just 1 parameter is called default constructor else its parameterized constructor.
if you make two constructors in same class then the one that matches your args will be executed.


**********ATRIBUTTES:-********** 
object attribute - the attribute that is different for all objects, usually defined with self.attribute , like name in above example.
class attribute - now if multiple objects have same attributes its foolishness to define them separately as it will consume space, so we use class attribute. 

_** #creating class:- 
class Student:              #class's name is generally started with a capital letter
    college_name = "NITJ"
    # constructor ->init
    def  __init__(self , fullname , crazy):
        self.name=fullname
        self.wth = crazy
        print("hello")

we can either write s1/s2.college_name in just student.college_name in below example
#creating object:-
s1= Student("karan" , "me");     # creates object named karan and assigns value to variable( second argument of init                     output:-hello
s2=Student("harpreet" , "you")                                                                                                                   karan
print(s1.name)                                                                                                                                   me
print(s1.wth)                                                                                                                                    nitj
print(s1.college_name);                                                                                                                          nitj          
print(s2.college__name);                                                                                                                        
**

obj attribute have more precedence than class attribute i.e, if there are class and obj attriburte with same name obj attribute will be considered.

**********METHODS**********
methods are function written in class, they are meant for working of objects 
the first argument in this function is always 'self' doesn't matter you use it or not.

class Student:              #class's name is generally started with a capital letter
    college_name = "NITJ"
    # constructor ->init
    def  __init__(self , fullname , crazy):                                                                output:- 
        self.name=fullname;                                                                                    hello 
                                                                                                               hello
        self.wth = crazy
        print("hello")
    def hello(self):
        print("hello")
Student.hello()

------------------------------

class Student:              #class's name is generally started with a capital letter
    college_name = "NITJ"
    # constructor ->init
    def  __init__(self , fullname , crazy):
        self.name=fullname;
        self.wth = crazy
        print("hello")
    def hello(self):
        print("hello")
    def name(self):
        return Student.name

Student.hello
#creating object:-
s1= Student("karan" , "me");     # creates object named karan and assigns value to variable( second argument of init
s2=Student("harpreet" , "you")
print(s1.name);


assignment 1:- create a class that takes name and marks of 3 subjects as argument in constructor and create a method to find average of all marks.

class student:
    def __init__(self, name, list):
        self.name=name
        self.marks1=list[0]
        self.marks2=list[1]
        self.marks3=list[2]
    def average(self):
        return (self.marks1+self.marks2+self.marks3)/3

s1= student("harpreet", [98,97,92])
s2=student("haramrit" , [12,12,34])
s3=student("sumeet" ,[11,9,16])
s4=student("deepanshu",[8,17,45])
print(s1.average())
print(s2.average())
print(s3.average())
print(s4.average())



STATIC METHOD - we have seen functions where we don't need self but we have to pass it in arguments or else it will return error , to solve this problem we use static method.
when do we actually need self- when we do things at object level , or use attribute of object hence,we can declare the method at class level, i.e, common for all.


class student: 
    @staticmethod        #decorator - changes the behavior of normal function 
    def college():
        print("NITJ")

----------------------------------------------------------------------------------IMPORTANT----------------------------------------------------------------------------------------

ABSTRACTION
user will see only the main part and not the implmentation

like in this code snippet the user will only see what is happening and not how its happening i.e, how variables are changing and all.
class car:
    def __init__(self):
        self.acc=False
        self.brake=False
        self.clutch=False
    def start(self):
        self.acc=True
        self.brake=True
        print("car started")
c1=car()
c1.start()


ECAPSULATION
here we make it such that the method and attribute both are part of same object/capsule
we've been doing this in almost all above snippets


assignment 2:- make a banking system with 3 methods- credit, debit and get_balance
class bank:
    def __init__(self,balance , account_no):
        self.balance=balance
        self.account_no = account_no
    def credit(self, amount, account_no):
        if(account_no != self.account_no):
            print("wrong account number")
            return
        self.balance=self.balance+amount
        print(self.balance)
        return
    def debit(self,amount , account_no):
        if(account_no!= self.account_no):
            print("invalid account number")
            return
        self.balance=self.balance-amount
        print(self.balance)
        return
    def get_balance(self):
        print(self.balance)
        return
a1=bank(10000 , 4567)
a1.credit(5000, 4567)
a1.debit(2000, 5769)
a1.get_balance()


# PRIVATE:- 
when you want a specific method and function to work only inside class and not be available outside the class.
use __ in front of any method or attribute name to make it private
methods can be used inside the class as usual but not outside

class bank:
    def __init__(self,balance , account_no):
        self.balance=balance
        self.__account_no = account_no
    def verify(self,account_no):
        if(account_no== self.__account_no):
            print(self.__account_no)
a1= bank(10000 , 8765)'
a1.verify(8765)
print(a1.__account_no)


# INHERITANCE 
taking properties/ methods from another class





