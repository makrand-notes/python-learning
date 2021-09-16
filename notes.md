Class and Object Declaration

    class Person:
    def __init__(self, name):
        self.name = name
        
    class Player(Person):
  
    def __init__(self, country):
        self.country = country
        
person = Person('ravindra')
player = Player('india')

To make a instance variable private, use double underscore

    class Player(Person):
      
        __sport = 'cricket'
        
There are getter and setter methods which can be used like this : 


    class Player(Person):
    
        __sport = 'cricket'
        
        def get__sport(self):
          return self.__sport
          
Private members are accessble via names mangling using format _className__membername :

    print(object.Player__sport)

To declare abstract class and methods, you need to import ABC(Abstract Base class) and abstractmethod

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

