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
    participants - ManyToMany relations with User (One user may participate in many rooms and one room may consist many users),
    updated,
    created 
    
    
class Message(models.Model):
    user - ForeignKey from User,
    room - ForeignKey from Room ,
    body,
    updated ,
    created 
    
 -------------------------------------------------------------------------------------------------------------------------------------------------------------------
Description : 
The main page shows a study rooms. Users may search for rooms by topic (click on topic row ) or by enter (partial) room name/room description in the search box.
The recent activity is shown in the right column (including room name, time and user). 
After registration every user has his own profile page (shown to everybody) and may update it.  
Every registered (and loged in) user may Create, Read, Update, Delete a study room and post comments (may delete his own comments).


