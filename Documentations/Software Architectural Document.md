# Software  Architecture  Document (SAD)
![SAD-TEAM5](https://cdn.discordapp.com/attachments/1061775332039987241/1061775442182422538/sad.jpg)
## Description of the conceptual design of the architecture

Dentistimo is a distributed system with a monolithic database that consists of 4 components that are connected through MQTT. Below is a detailed description of each component and thier responsibilities:

 
**User Interface:** This component enables the user to interact with the system via graphical user interface. We used NodeJS to create the website and VUE.js to design the interface. To display the dentist locations on a map, we used leaflet. The component utilizes the Vuex library to create a session for the logged in user.

**Booking handler:** This component is responsible for checking if a timeslot selected by a user is available. Before approving a new booking, it double checks in the database the availability of selected date and time. When a booking is successful, it is stored in the database and an email confirmation to the user and the user receives an email confirming their appointment booking, to make this possible we use nodemailer. It is also responsible for getting specific users appointments as well as deleting them upon request. This component has a circuit breaker that is implemented using the opossum library. To test fault tolerance, we used a MQTT Box to perfom a load test where we sent 100 booking requests to the component.


**Dentist Handler:** The dentist handler is responsible for fetching dentist data from the dentistry Json file using node fetch and saving it to mongoDB without duplicates. In addition, when it receives requests from the user interface to either get all dentists or get a specific dentist by id, it searches for it in the database and if successful, it sends back a response with the results.

**User handler:** The user handler is responsible for handling user information sent to it by the user interface component. It is responsible for creating a new user and when successful an email confirmation awaiting verification is sent to the user using nodemailer. When an existing user signs in, it handles the authentication by matching provided data with data saved in the database.Moreover, it is responsible for getting user’s information, editing user information.

  

## Architecture styles

We used a mix of different architectural styles such as publish-subscribe style, pipes and filters, as well as a
layered architecture. To achieve this, we choose to use the service based architectural style:

  
**Layered architectural style:**
The Presentation layer which is the user interface. It will use a websocket to send and receive MQTT
messages. The business logic is composed of independent components: the user handler, Dentist handler and
booking component.They communicate with the frontend on the presentation layer through a broker(MQTT)
which is the middleware. The data layer has a monolithic database as well as the Dentistry JSON file.

**Publish-subscribe architectural style:**
To enable connection between the components on the business logic layer and the presentation layer,
We used a publish-subscribe architectural style. The messaging between the subscribers and the publisher
occurs via MQTT. Subscribers in our system will receive all messages published to the topics to which they are
subscribed to. The publisher is responsible for defining the topics to which subscribers can subscribe.

 
**Pipes and filters:**
In our distributed system, the MQTT broker will act as the pipe, and the components will act as filters which
process different kinds of data that it received. The pipe (MQTT) connects the filters(independent components on the business logic layer). Messages/payload is passed through the pipe to adjacent filters. The pipe and filter style will enable the incoming payload to be filtered, such that the relevant changes can be displayed on the screen.

## How the conceptual design is mapped onto implementation/technologies.
Our project involves creating a service that allows residents of Gothenburg to book dental appointments through a graphical user interface. The system should allow users to find available appointment times within their desired time window and receive confirmation or rejection for their booking. We are using the Vue framework for the frontend and Node.js for the backend, as our team has experiences with these technologies.


The Presentation Layer is both the starting and ending points of the data flow within our system. The component diagram above depicts the direction that the messages are transported within the system. Activity on the user interface triggers the system. The user interface uses a websocket which allows it to send and receive MQTT data from the server directly into the web browser. The MQTT broker that we are using is HiveMQ cloud. It is not directly connected to the database, but instead communicates with the business logic components that retrieve data from the database as needed.


The components of the business logic are independent thereby achieving a minimal coupling between components. The messages that the components on the business logic receive from the user interface are usually requests. The appropriate component responds by subscribing to the published topic. It handles the request and publishes the results back to the user interface. On the data layer, only the dentist handler communicates with the dentistry registry JSON file and saves the data to the database. All the components on the business logic communicate with the database.


One of the important aspects we considered when choosing which technologies to use for implementation was familiarity. Even though there are other technologies that might better suit the system. We chose to work with technologies that we have all used before and are comfortable with. Since the system has to be delivered by a certain date, we did not feel that we had the time to properly research and learn new technologies.


## **Architecture design decisions and tactics used**

 **1. Design Decisions**

 - Separation of concerns(SoC):

Our distributed system consists of 5 components. Each component is separate and independent from the other components, making each component a separate working repository. This way we can accomplish the separation of concerns and  the single responsibility by separating the application into distinct sub-units, so each sub-unit addresses a separate concern, and by that achieving a minimal coupling between the different components.

  

 - Quality of service

We have decided to use QoS 1 for sending and receiving all MQTT messages within our system. QoS 1 guarantees that a message is delivered at least one time to the receiver. The messages can be sent or received multiple times which reduces the risk of data loss, as compared to QOS 0 which works on the "fire and forget" principle which means that delivery is not guaranteed and few messages are lost occasionally. QOS 0 would not be acceptable in our case because all the messages that are being sent and received are important.

Futhermore, speed is of importance and sending/receiving the same message multiple times does not affect our system, we think speed will contribute to a better and faster user experience and therefore, we deduced that using QoS 1 for the whole system would be more suited for our case as compared to QOS 2.

**2. Architecture Drivers**

  

***User experience***, When designing the system, user experience was an important aspect to keep in mind because we did not want users to face problems while using a website's user interface. Therefore, ***usability*** is an important architectural driver. The system should allow a user regardless of computer literacy to easily navigate the application and achieve their goal of booking an appointment.

Furthermore, the system must be available and operating properly when it is requested for use. ***Availability*** is an architectural driver for the system because it would be inconvenient for potential patients that are in desperate need of a dentist appointment if there is a risk that the system is not operational at certain times. The system should be designed to endure any system faults so that the system remains compliant with its specifications and we do this by using a circuit breaker on the booking component.


Moreover, ***reliability*** is an important architectural driver because it is crucial for both the clinics and the users that the information that is shown through the graphical user interface is correct. The system should be failure-free when it comes to appointment booking, and it does this by not overbooking a time slot at a clinic.

  
  
  

 **3. Design Tactics**

  

 - Modifiability and Maintainability:

The system should be receptive to change. We do this by using different subunits to do specific tasks which will make it easy for us to modify and maintain the system to for example meet new requirements without affecting the system as a whole as they will be limited in scope.

- Interoperability:  

Interoperability is an ability of one system to interact with another system. Because we have a distributed system, different components need to communicate and exchange information with one another. We achieve this by using a MQTT broker.

 - Fault tolerance:

Considering we will have several components communicating with each other, and as the number of interactions between the components increases, the chances of possible failures also increases in the system. The solution is to use fallback to avoid that, which can be achieved by using a circuit breaker pattern that wraps requests and detects when any component fails. For example if a failure is detected, the request returns an error message instead of sending a request to a failed component.

  

We selected the booking as the component to implement fault tolerance on. The circuit breaker protects the component from being spammed with multiple bookings while already being unavailable due to bookings exceeding a specific number per second.
