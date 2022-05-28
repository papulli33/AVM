# Malls of Ankara
> Location data of the shoping malls which are in  Ankara.
> Live demo [_here_](<https://osgeo-team-15.herokuapp.com/>).


## Table of Contents
* [Introduction](#introduction)
* [Technologies Used](#technologies-used)
* [Setup](#setup)
* [Understanding The Project](#understanding-the-project)
* [Usage and Feature](#usage)
* [Possible Uses for the Project](#possible-uses-for-the-project)
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)


## Introduction:
### Project Aim & Goals
This project was designed and created for the users to get the location of Ankara's Malls. Its purpose is to make it easier for people to locate malls' location and also make it easier to analyze malls location so that it can be used for GIS purposes in the future.



## Technologies Used
- **PostgreSQL 11.5**

![image](https://user-images.githubusercontent.com/92017528/170726537-3822f266-9e1e-4322-b8d2-4a575828631e.png)

  PostgreSQL is an open source and completely free object-relational database system with powerful features and benefits. Taking advantage of the security,       storability and scalability features of the SQL language, PostgreSQL is also used as a database manager in many areas.

- **OpenLayers**

 ![image](https://user-images.githubusercontent.com/92017528/170726698-866a509c-fcdd-4086-a891-f942367055bc.png)

  OpenLayers is a simple open-source JavaScript library with no server-side dependencies that allows us to develop functional map applications to display map data in most modern web browsers.

- **Visual Studio Code**

![image](https://user-images.githubusercontent.com/92017528/170726621-1f3de579-422e-4ef2-acbe-4065236fbded.png)

  Visual Studio Code is a source-code editor made by Microsoft for Windows, Linux and macOS. Features include support for debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git. Users can change the theme, keyboard shortcuts, preferences, and install extensions that add additional functionality.
- ***QGIS 3.24***

![image](https://user-images.githubusercontent.com/92017528/170726813-b0b5c7bd-8b5e-4ee4-b890-3819415b3e35.png)

  QGIS is a user friendly Open Source Geographic Information System (GIS) licensed under the GNU General Public License. QGIS is an official project of the Open Source Geospatial Foundation (OSGeo). It runs on Linux, Unix, Mac OSX, Windows and Android and supports numerous vector, raster, and database formats and functionalities. 
- ***Syncthing***

![image](https://user-images.githubusercontent.com/92017528/170726875-10c91ea2-8f68-4ca2-90c1-6a231a71a63c.png)

  Syncthing is a continuous file synchronization program. It synchronizes files between two or more computers in real time, safely protected from prying eyes. Your data is your data alone and you deserve to choose where it is stored, whether it is shared with some third party, and how it's transmitted over the internet.
- ***NodeJS 12.13.1***

![image](https://user-images.githubusercontent.com/92017528/170726946-3cdca527-e1d4-4cac-bae3-043ccc930227.png)

 Node.js is an open-source, cross-platform, back-end JavaScript runtime environment that runs on the V8 engine and executes JavaScript code outside a web browser.
- ***PostGIS***

![image](https://user-images.githubusercontent.com/92017528/170726992-ec116bc3-a0e6-4a65-bc88-d48da305e792.png)

 PostGIS is a spatial database extender for PostgreSQL object-relational database. It adds support for geographic objects allowing location queries to be run in SQL.
- ***QField 1.2.0***

![image](https://user-images.githubusercontent.com/92017528/170727062-ffe0e39c-96f6-4cfb-9907-5bd3b5e21cb5.png)


 QField is an open-source solution for mobile data collection for Android, iOS, and macOS. It’s built by the QGIS team
- ***Google Maps***
  Google Maps is a web-based mapping service provided by the company Google. This mapping system allows users to quickly access information about any country, city, neighborhood, or even street in the world.We used the google map application to find the locations of the awms in Ankara in the project. We found the awm locations we found in QGIS and marked them.



## Setup

- Install Visual Studio Code on your computer. Download [_Visual Studio Code_](<https://code.visualstudio.com/download>)
- Install Node.js on your computer. Download [_Node.js_](<https://nodejs.org/en/>)
- Select all the options that will appear during the Node.js installation.
- After installing Node.js, npm should also be downloaded to your computer by the virtue of Node.js installation. 
  


***There is also some JavaScript packages need to be installed with our new Node.js module . And these packages will be installed via npm command. Packages to install are listed as follows:***

### Express Module
Express is a  Node.js web application framework that gives quality features to develop our applications.
And we install it by typing "***npm install express --save***" 
### File System Module
This package allows you to work with your computers file system.
And we install it by typing "***npm install fs --save***" 

### Bluebird Module
Bluebird is a library which has diffrent features and improves performance.
And we install it by typing "***npm install bluebird --save***"

### Pg-Promise Module
Pg-promise is a PostgreSQL interface for NodeJS.
And we install it by typing "***npm install pg-promise --save***"

To check if the website is working or not. Type  "***node index.js***",in your terminal and press your enter key.
After that go to your web browser of choice and  and type: ("***http://localhost:4000/***"). Now you can see our Project in your local server and you can also see the text data by going to "***http://localhost:4000/api/data***"


## Understanding The Project

This is our main project directory, the files and folders we are interested in order to understand the project briefly are in here.

![image](https://user-images.githubusercontent.com/92017528/170716573-b946503e-ad00-483d-89e1-b33e79ad65fa.png)

appConfig.js is a javascript file which contains our database connection settings.

database.js is retrieves the data which is stored on the database. 

index.html handles the background map creation which is obtained from OpenLayers and basic website design then it also receives query responses via Jquery. We also implement HTTPS protocol here so our site is safe to use with encryption.

index.js allows us to publish our website through NodeJS.

After implementing the code we connect our database to QGIS so we can get realtime photos to from your phone via QField.

We manage our points by connecting our database to QGIS and changing its value relations properly.After that we send our QGIS Project to our phone and open it on Qfield

![image](https://user-images.githubusercontent.com/92017528/170718921-7e580d61-0f33-42da-be1a-d9ae14b0de20.png)

(awm must be AVM but its to expected when you type it hastily last minute)

***Why We Need Syncthing***

Syncthing allows us to a continuously synchronize our files between our phone and computer.Since we need to collect data in real time in this project we need to use Syncthing with QField which allows us to make changes to our QGIS project from anywhere if we have an internet connection and a good GPS signal.

![image](https://user-images.githubusercontent.com/92017528/170778631-c3fe0815-fd6b-45d5-a16b-a5a578e194a7.png)

We get the the location of the Mall from our GPS and add number of shops inside of the mall,and its photo to our database from QField.

## Usage
Its features and usage are listed here:

- General view of the website.

![image](https://i.imgur.com/DDirpUh.png)

- You can go to Hacettepe University's website by clicking the logo on the navbar.

![image](https://i.imgur.com/eH8z7tv.png)

- If you click on the 'Contact us' button on the far right of the navbar, you can find the source code of the project, its descriptions and the contact information of the project designers.

![image](https://i.imgur.com/CKMyB8I.png)

- Icons show the mall in Ankara and OpenLayers helps find spots.

![image](https://i.imgur.com/EsuKnoQ.png)

- There is a message box in the footer that explains the site in a simple way for users.

![image](https://i.imgur.com/i7ZvwOh.png)

- The address of the departments of those who designed this project is shown on Google Maps in the footer.

![image](https://i.imgur.com/ATPSHYa.png)

- The names of the designers and developers are shown on the cards.

![image](https://i.imgur.com/FXs2fkh.png)


## Possible Uses for the Project

- If you need to do an GIS project you can use the given location data and add new attributes to it via QField on the field or via QGIS and since you also have the abilty to the add points via QField and QGIS you can add more points to make your projects scope bigger.
- If you don't need to do any GIS application you can observe the mall's location data from the map or simply import the spatial data from the site to quickly get coordinates of the maps.

## Project Status
Project is: |***COMPLETE***|


## Room for Improvement

Room for improvement:
- The Project needs to improve in UI deparment which helps makes it easier to understand for the end user like Pop-Up Tabs and easy searching function inside the site. 
- We can add more attributes to the malls since it only has Number of Shops as its attribute. 


## Acknowledgements
- This project was based on [this tutorial](https://wiki.osgeo.org/wiki/Training_Material_for_2019_UN_Open_GIS_Challenge_2_-_Open_geospatial_data_and_software_for_UN_SDG_16,_Peace_justice_and_open_institutions).



## Contact

| Team Members | Account | Link | 
| ------ | ------ | ------ |
| Ümmü Sude YILDIRIM|LinkedIn |https://www.linkedin.com/in/sude-yildirim-6923591a3/ |
| Mertcan ERDEM | Mail | merterdemcan@hotmail.com|
