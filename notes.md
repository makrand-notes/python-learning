### Class and Object Declaration

    class Person:
 
    def __init__(self, name):
        self.name = name
        
    
    class Player(Person):
  
    def __init__(self, country):
        self.country = country
        
person = Person('ravindra')
player = Player('india')

There are some predefined attributes in each class containing meta information
1. __dict__ : stores class' namespace
2. __doc__ : documentation string(declared inside class definition) 
3. __module__ : module in which class is defined
4. __name__ : stores class' name
5. __bases__ : stores all base(parent) classes of given class

### Attributes:

There are two kind of attributes - class attributes and object attributes. Class attributes are shared by all objects from that classz(like static instance variables in java) where as object attributes are specific to that instance

You can refer class attribute using both class reference or object reference. However is you update the value using object reference, value will only change for that specific instance. 

e.g 
class Animal:
    name = "animal"
    
dog = Animal()
cat = Animal()
Animal.name = 'abc' will change for both instances dog and cat. 

However cat.name = 'cat' will not change animal name for dog object. 

To make a instance variable private, use double underscore whereas to make it protected use single underscore(_). You can also use __ to make methods private as well. 

    class Player(Person):
      
        __sport = 'cricket'
      
Names Mangling : Private members are stored in the format _classname__membername 

### Method:

First parameter in any method is always self

Methods can be used to add new attributes to object e.g. Animal class doesn't have color attribute but can be added using :

    def add_color(self, color):
        self.color = color

Constructor is declared with name  __init__ 

First parameters in constructor is always to hold the instance reference

There are getter and setter methods which can be used like this : 

    class Player(Person):
    
        __sport = 'cricket'
        
        def get__sport(self):
          return self.__sport
          
Private members are accessble via names mangling using format _className__membername :

    print(object.Player__sport)
    
super() is a special function to access base class' attributes or methods

isinstance() and issubclass() are function provided to check inheritence relationship between two objects

Base and derived class declartion syntax : class childClass(BaseClass) e.g. class TennisPlayer(Player):

Python supports multiple inheritence

class Faculty(Employee, SME):

Method/Attribute resolution happens from left to right i.e. if same attribute is present in both base classes then Employee would be considered

To declare abstract class and methods, you need to import ABC(Abstract Base class) and abstractmethod

from abc import ABC, abstractmethod

    class Bike(ABC):
    
        @abstractmethod
        def run(self):
            pass
            
    class Pulsar(Bike):
        def run(self)
            print('this is pulsar implementation')
            
    classs Honda(Bike)
    
        def run(self):
            print('This is honda implementation')
           
Abstract classes can not be instantiated

To declare an enum you need to use : import enum 

class GuitarType(enum.ENUM):
    ACOUSTIC, ELECTRIC, UNKNOWN = 1, 2,3


Python does not support overloading by default. For a class all the data members and methods that we declare are stored in a class object as an attribute. An object can have only 1 attribute of given name
