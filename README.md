# T-5-Documentation

## Table of Contents
- Description 
- Components
- Sub-documents
- Team Members
- Team Resources
- Software Technologies


## Description
Dentistimo is a web application that allows the residents of Gothenburg to  choose a dentist from the map and book dentist appointments with ease. 
Dentistimo is a distributed system made of 5 components. The system's components are communicating with each other through an MQTT middleware by sending and receiving lightweight messages, and our main goal is to create a responsive interface frontend accessing different functionalities that supports communication over MQTT using protocol through a websockets, which will allows the asynchronous communication with the server. 


## Components:
- [User interface](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface):This component allows users to interact with the system.
- [Booking Handler ](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler):When a user makes a valid appointment,  this component creates the new booking and stores it in the database.
- [Dentistry Handler ](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-dentisthandler):Responsible for fetching dentist data from dentistry Json file and publishing the data to the frontend map for the user to see the dentists in Gothenburg.
- [User Handler ](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler):Responsible for fetching user data from the database and publishing the data to the frontend for the user to see their personal information and update it if needed.
- [Timeslot Generator ](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-timeslotgenerator):This component is responsible for creating time slots for the dentistry based on its opening hours and availability.


## Sub-documents

- [Purpose](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-documentation/-/blob/main/Documentations/Purpose.md)
- [Project Management Report (PMR)](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-documentation/-/blob/main/Documentations/Program%20Management%20Report.md)
- [Software Requirement Specification (SRS)](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-documentation/-/blob/main/Documentations/Software%20Requirement%20Specification.md)
- [Software Architecture Document (SAD)](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-documentation/-/blob/main/Documentations/Software%20Architectural%20Document.md)



## Team Members

- Akuen Akoi Deng 
- Cynthia Tarwireyi
- Jonna Johansson
- Kanokwan Haesatith
- Marwa Selwaye
- Nazli Moghaddam
- Sergey Balan

## Team Resources

- Trello board
- Google drive

## Software Technologies
 
- HiveMQ
- Vuejs 
- BootstrapVue
- Nodejs 
- JavaScript
- Mongoose
- Node package manager
- MapBox and leaflet
