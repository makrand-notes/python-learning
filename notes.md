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

