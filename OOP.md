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
        self.name=fullname;
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

**********METHODS***********











