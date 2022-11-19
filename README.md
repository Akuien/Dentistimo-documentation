# T-5-Documentation

## Table of Contents

- Purpose 
- Team Members
- Team Resources]
- Software Requirement Specification (SRS)
- Software Architecture Document (SAD)
- Program Management Report (PMR)

## Purpose
The purpose of this system is to allow the residents of Gothenburg to book a dentist appointments with ease. 

## Description
Let people know what your project can do specifically. Provide context and add a link to any reference visitors might be unfamiliar with. A list of Features or a Background subsection can also be added here. If there are alternatives to your project, this is a good place to list differentiating factors.

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

## Software Technologies
 
- MQTT-broker
- Vuejs 
- BootstrapVue
- Nodejs 
- JavaScript
- Mongoose
- Node package manager
- MapBox GL 


## Software Requirement Specification (SRS)

link to SRS

## Software Architecture Document (SAD)

# Architecture Styles
- Publish-subscribe architectural style:                                                                                                                                                                                 
In order to make a connection between different components in the system we can use
publish-subscribe architectural style. Publisher will publish messages to a topic and subscriber                
or multiple subscribers subscribes to a topic on multiple topics. When messages come into the topic, they are sent out to the subscribers of the topic.When we talk about messages, in our case it can be the data about the appointments in dental registry or an operation that can be relevant  to the subscribers such as sending a request for making an appointment. The messaging between the subscribers and the publisher is via a broker which in our case is MQTT. In our design, the MQTT is going to be used as the network protocol between our FrontEnd and BackEnd(in this case the different subsystems). The various subsystems will share data and resources to each other by publishing and subscribing to topics through the MQTT.

- Pipes and filters:

In our distributed system, our components will act as filters which process different kinds of data
that it received from the MQTT broker which will act as pipes.

- Client-server:

Dentistimo is a web-based application where requests are sent from the web interface
(the frontend) where the different users; the general users(patients) and the clinic officers or dentist 
sends their requests to the backend which then sends back the response.

- Layered architectural style:
The layered architecture where we have the Presentation layer which is the user interface/frontend. 
The Business logic which is the middle layer in our case composed of the different subsystems which communicate with the frontend and share resources and data with each other through a broker(MQTT) which could be viewed as the middleware. The third layer which is the persistent layer composed of the common single database to be 
shared by all the subsystems in the whole distributed system.

# Design Decisions

- Separation of concerns(SoC):
The team decided based on the requirements given in the guideline, that our system
is to be composed of  more than 4 components, where each component
is separate and independent from the other components, making each component a 
separate working repository. This way we can accomplish the separation of concerns 
and the single responsibility by separating the application into distinct sub-units, 
so each sub-unit addresses a separate concern, and by that achieving a minimal coupling
between the different components.

# Architecture Drivers

- Modifiability: 
In order to create an interface which is easy to use for making appointments, we have to keep the 
design simple to increase modifiability. Everyone should be able to book an appointment without 
any difficulties. we can adapt this characteristic by using effective navigation and simple forms
for users to fill out when we want them to add their information. Also due to using different 
subunits to do specific tasks or concern, it makes it easy for us to make modification on any 
subsystem without affecting or changing the others.

- Maintainability: 
The system should be maintainable, meaning that it should be able to handle changes such as
introduction of new features during and/or after development. We should be careful about the 
obstacles along the way, and also we should take into consideration the amount of time we might 
need to spend on fixing the errors or any kind of malfunction. Having a distributed system allows
 for easier maintainability of components.

- Availability: 
Users need to be able to use the system at all times. The system should be designed to endure any 
system faults so that the system remains compliant with its specifications. Fault detection tactics 
such as Ping/Echo that its mechanism is based on asynchronous request/response pair exchanging 
active nodes can be used.

- Fault tolerance: 
Considering we will have several components communicating with each other, and as the number of interactions between the components increases, the chances of possible failures also increases in the system. The solution is to use fallback to avoid that, which can be achieved by using a circuit breaker pattern that wraps requests and detects when any component fails. For example if a failure is detected, the request returns an error message instead of sending a request to a failed component.

## Components

# the system consists of 6 components: 
- User Interface
- User Hanlder
- Dentistry Handler
- Timeslot Creator
- Availability checker
- Appointment Handler

## Program Management Report (PMR):

Link to PMR

## Installation
Within a particular ecosystem, there may be a common way of installing things, such as using Yarn, NuGet, or Homebrew. However, consider the possibility that whoever is reading your README is a novice and would like more guidance. Listing specific steps helps remove ambiguity and gets people to using your project as quickly as possible. If it only runs in a specific context like a particular programming language version or operating system or has dependencies that have to be installed manually, also add a Requirements subsection.
