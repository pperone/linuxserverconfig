# Udacity Linux Server Configuration Project

Final project in the Full Stack Web Development Nanodegree. Preparing and deploying the python app created in Project 3 (Catalog) to a Linux server.


## Information

#### IP Address
52.2.81.246

#### URL
The app can be accessed at http://52.2.81.246.xip.io/

#### App
The application is a catalog of bands, separated by categories and with a summary attached to each.

#### Tools
The server for the application is an instance from the Amazon Lightsail Web Service (Ubuntu machine). The application uses the Flask framework, and some additional modules incorporated were:

- psycopg2 (for managing the Postgresql database)
- oauth2client (to implement the Google login)
- sqlalchemy (to deal with the database creation and management within the python app)

#### Configuration Steps
Upon the creation of the AWS instance, some configuration of the server was necessary, mainly:

- Creation of an user named "grader", and the subsequent addition of sudo privileges and public key to ssh into the server.
- Alteration of the timezone to UTC
- Configuration of UFW to allow for the required ports
- Change of ssh port to 2200
- Installation of apache2 to serve the application
- Installation of virtualenv to install the necessary modules in a sandbox environment
- Creation of the necessary apache configuration and wsgi files for the application

#### Additional Information
A user named "grader" was created, and the key to ssh to it was provided in the notes to the reviewer. Also, the required "catalog" database was created, and the password to access it was also added to the notes.
