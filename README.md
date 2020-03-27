Go Working
===

System to aid control of desks and rooms at Fábrica do Futuo's Go Working.  

Copyright (C) 2019-2020 Fábrica do Futuro  

This program is free software: you can redistribute it and/or modify  
it under the terms of the GNU General Public License as published by  
the Free Software Foundation, either version 3 of the License, or  
(at your option) any later version.  

This program is distributed in the hope that it will be useful,  
but WITHOUT ANY WARRANTY; without even the implied warranty of  
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the  
GNU General Public License for more details.  

You should have received a copy of the GNU General Public License  
along with this program.  If not, see <http://www.gnu.org/licenses/>.  

i18n
---

* [English](./README.md)  
* [Português Brasileiro](./README.pt.md)  

---

RGSoC 2020
---

This project is part of Rails of Girls Summer of Code 2020. The offical 
page for this project is at the 
[RGSoC Teams App](https://teams.railsgirlssummerofcode.org/projects/366-improve-the-desks-and-rooms-control-system-for-the-coworking).  

### Description

The "Go Working Map" started as a web form to aid the control of the 
desks at 
[Fábrica do Futuro's Go Working](https://fabricadofuturo.com/en/#terreo). 
Then it evolved to a system where all inhabitants of 
[Fábrica do Futuro](https://fabricadofuturo/en/) could find information 
of each other's startup and business, effectively providing a virtual 
place as a means for exchanges. Go Working is how we call Fábrica do 
Futuro's coworking space.  

Because the project wasn't meant for this purpose, the code - originally a 
simple collection of Flask-WTF html forms - needs refactoring. The current 
code base is not suited for the stakeholder's demands on the project.  

Ideally the website should be able to include more information about 
[Fábrica do Futuro](https://fabricadofuturo.com/en/)'s inhabitants. People 
should be able to update their own information and share it with others, 
pretty much like a regular social network. End users should be able to 
request additional functionality and the scope of the project shall be 
easily expanded on demand.  

Also we are working on a better way for inhabitants to schedule rooms for 
meetings. This is needed because there are so many meeting rooms and many 
people doing meetings all day long. We hope to integrate this functionality 
in the Go Working Map.  

This is part of a bigger system to improve the daily experience for 
inhabitants of 
[Fábrica do Futuro's Go Working](https://fabricadofuturo.com/en/#terreo). 
The primary goal is to directly benefit innovative startups sited at Porto 
Alegre at [Fábrica do Futuro](https://fabricadofuturo.com/en/). Since this 
is a Libre Software project, the secondary aim is to provide technology to 
co-workings worldwide, hopefully achieving three goals: influencing the 
mindset and daily routine of co-workings and similar spaces; contributing 
to the startups community; benefit from other like minded people's 
contributions; and therefore aiding startups in general. Your own startup 
is next? :)  

[Fábrica do Futuro](https://fabricadofuturo.com/en/) has infrastructure at 
Porto Alegre - Brasil to house the team working on the project so the team 
will be directly affected by this project, at least temporarily 
*- but you're welcome to stay here after the SoC! ;) -* so we would expect 
from the team much feedback on the system and that you participate on 
defining it's scope and suggest new functionalities, even if they will have 
to be implemented by others.  

Team will have full access to the 
[Fábrica do Futuro's Go Working](https://fabricadofuturo.com/en/#terreo) as 
if they were inhabitants. This includes but is not limited to electrical 
and caffeine power, access to high speed wireless internet (and by July 
gigabit ethernet on all desks), bathrooms, showers, meditation room, call 
booths, meeting rooms, living spaces, a retro games emulator and happy 
smiles everywhere.  

### Tasks and features

Things that should be done:  

* The project needs someone  who can research and implement a proper 
[ACL](https://en.wikipedia.org/wiki/Access-control_list) which will be 
responsible to enforce the business rules to display information to logged 
in users;  
* Personal information of companies and individuals should be stored and 
used respecting the Brazilian pertinent legislation the 
[LGPD](http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/L13709.htm). 
We have mentoring on that, you don't need to do legal research;  
* We currently only have a web interface built on Flask itself. It would be 
nice to have an Android/iOS application that we could provide to people who 
prefer that interface, but that is not the main goal;  
* Users requested some sort of job board so startups could advertise to 
each other (or maybe externally?) with what and how they need help. Perhaps 
you could help to make the very code that will help you find your next 
contractor or business partner ;)  
* There is another team working on a React Native app/web frontend for the 
rooms schedule module. The task in hand is to provide an API 
([Flask](https://flask.palletsproject.com)/RESTful preferred but not 
demanded) for the apps to consume, as well as interact with the 
[Google Docs API](https://developers.google.com/docs/api) which will act 
both as a database and an alternative form of end users interacting with 
the system.  

Don't worry about taking care of all these tasks. You may freely select 
which ones you feel more comfortable working on. You may even propose other 
tasks and if they make sense, we can change the scope of the project 
accordingly.  

### Requirements

The mentor of the project prefers Python/Flask because he is familiar with 
the technology and the current code is already written using the 
[Flask](https://flask.palletsproject.com) framework. But if the team 
chooses it can use other programming language such as Javascript or Ruby on 
Rails, or even other Python framewroks such as Web2Py, Py4Web or Django. 
This part of the project still has no code, therefore there's enough 
freedom to adapt it yet.  

The project should be written in a way that will allow other integrations 
in the future, and should be agnostic in the sense of needing little work 
to change the database or frontend integrations. This is easily 
accomplished using tools such as Flask-SQLAlchemy, but alternative 
solutions are welcome.  

### Tags

Python, Flask, LGPD, Jinja, Bootstrap, MySQL, SQLAlchemy, Google Docs  


Releases
---

### v 0.1

Delivery date: Friday, December 06, 2019

#### Scope

* End Users should be able to view the goworking tables;  
* End Users should be able to see which chairs are occupied, for
   who, what company;  
* End Users should be able to edit information about chairs, people,
   companies;  

### v 0.2

Delivery date: Friday, December 12, 2019  

* All registrations working (inhabitants and companies, in addition to spaces,
   tables and chairs);  
* Updating data is not working properly. To change
   information,it is necessary to re-register;  

### v 0.3

Delivery date: Wednesday, December 25, 2019

* Editing inhabitants and businesses is working correctly;  
* Only relevant functions appear for End Users;  
* UX changes specific to Ethiele:  
  * When clicking on an empty chair, an add new button is displayed
     inhabitant with specific form for this purpose;  

### v 0.4

Delivery date: Friday, January 10, 2020  

* Correct display and recording of CPF and CNPJ;  

Roadmap
---

TODO:

- [ ] Document how to use with pipenv
- [ ] Increase the skeleton from 4 to 5 columns, add the cabins
- [ ] Extend the scope of the system with new blueprints to contemplate
   other features  
- [ ] Migrate login out of the goworking blueprint 
- [ ] Change filenames to eg :view_habitante.py,
  model_habitante.py, etc. 

Instructions
---

In the event that someone ever reads the installation instructions.  

### git

Clone the repository with the source code.

    git clone https://notabug.org/fabricadofuturo/goworking-mesas.git

### Prepare Python and Flask

I use *pipenv*. How to install pipenv is outside the scope of this guide.


    mkdir instance
    cp default_config.py instance/config.py
    cp default_env .env

Edit the `.env` and `instance / config.py` files with the configuration data
Flask, SQLAlchemy, WTForms, etc.  

The minimum required is to define the data in the database. For example, in
archive*.env*:  

    DATABASE_URL=mysql+pymysql://usuario:senha@localhost/goworking

    user@server:goworking-mesas$ pipenv install

### Database

You can use any type of database management system that
work with Flask SQL Alchemy. These instructions are for using MariaDB:  

#### Install MariaDB Server

MariaDB is the GPL version of MySQL.  
No debian: `sudo apt install mariadb-server`;  

#### Change username and password

Change the database creation file located at *doc/mysql.sql*:

    CREATE DATABASE goworking DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_bin;
    GRANT ALL PRIVILEGES ON goworking.* to usuario@'localhost' IDENTIFIED BY 'senha';

Change "user" to some username and "password" to any password.

#### Run creation script

Access mariadb-client, copy and paste the commands or run the script.

No debian: `sudo mysql`

    MariaDB [(none)]> SOURCE doc/mysql.sql;
    Query OK, 1 row affected (0.001 sec)
    
    Query OK, 0 rows affected (0.001 sec)
    
    MariaDB [(none)]> SHOW DATABASES;
    +--------------------+
    | Database           |
    +--------------------+
    | goworking          |
    | information_schema |
    | mysql              |
    | performance_schema |
    +--------------------+
    4 rows in set (0.001 sec)

If what you have available is a PHPMyAdmin or something, find out how it is
the hard way to paste these simple commands into this complicated system.

#### flask-migrate

    user@server:goworking-mesas$ pipenv run flask db init
    Loading .env environment variables...
    user@server:goworking-mesas$ pipenv run flask db upgrade
    Loading .env environment variables...
    INFO  [alembic.runtime.migration] Context impl MySQLImpl.
    INFO  [alembic.runtime.migration] Will assume non-transactional DDL.
    INFO  [alembic.runtime.migration] Running upgrade  -> fead50b08d21, empty message
    INFO  [alembic.runtime.migration] Running upgrade fead50b08d21 -> dc7d560eee94, empty message

### gunicorn

I use systemd.

There is an example systemd file in *doc/gunicorn-goworking.service*.

    user@server:goworking-mesas$ sudo cp gunicorn-goworking.service /lib/systemd/system/
    user@server:goworking-mesas$ sudo systemctl enable gunicorn-goworking.service
    user@server:goworking-mesas$ sudo systemctl start gunicorn-goworking.service

### Nginx

Sample file in *doc/goworking.conf*.  

    user@server:goworking-mesas$ sudo cp doc/goworking.conf /etc/nginx/sites-available/
    user@server:goworking-mesas$ pushd /etc/nginx/sites-enabled
    user@server:/etc/nginx/sites-enabled$ sudo ln -s ../sites-available/goworking.conf
    user@server:/etc/nginx/sites-enabled$ popd
    user@server:goworking-mesas$ sudo nginx -t
    nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
    nginx: configuration file /etc/nginx/nginx.conf test is successful
    user@server:goworking-mesas$ sudo systemctl -l reload nginx.service
  
  
---




