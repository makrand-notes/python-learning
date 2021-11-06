For building web application in python space you can use Django, Apache Flask or FastAPI. Django is good when we want to build a full fledged UI based web application but will have lot of boilerplat code. For simple backend services development better use Flask. Flask will outperfrom FasAPI when connecting to database. 

Flask is a micro web framework for python space. It doesn't have ORM or many other advanced features built in itself but it works with third party libraries to provide overall web application functionalities. 

Virutal environment is an isolated space for program execution where each virtual environment can have its own set of dependencies. So if there are n projects, each project can have its own set of dependency. 

We first need to install pip and virutal environment. After that create a virutal environment and then activate it. 

Steps for windows enviornment : 

1. py -m pip install --upgrade pip

2. Create a project directory using mkdir and cd into it

3. py -m venv env

4. .\env\Scripts\activate

5. pip install flask

6. pip install flask_sqlalchemy

7. pip freeze > requirements.txt



SQLAlchemy is an ORM tool to connect to database. 

