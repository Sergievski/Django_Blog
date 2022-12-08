# Django_Blog

--> Clone the repository using the command below :

git clone https://github.com/Sergievski/Django_Blog.git

--> Create a virtual environment :

python -m venv venv

--> Activate the virtual environment :

.\venv\Scripts\activate

--> Install the requirements :

pip install -r requirements.txt

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
Application Models : 
    
class User(AbstractUser):
    name ,
    email ,
    bio ,
    avatar 
    
    
class Topic(models.Model):
    name   


class Room(models.Model):
    host - ForeignKey from User,
    topic - ForeignKey from Topic ,
    name,
    description ,
    participants - ManyToMany Relations with User (One user may participate in many rooms and one room may consist many users),
    updated,
    created 
    
    
class Message(models.Model):
    user - ForeignKey from User,
    room - ForeignKey from Room ,
    body,
    updated ,
    created 
    
 -------------------------------------------------------------------------------------------------------------------------------------------------------------------

