# Purpose

## **Team members Roles, and Tasks**

All team members were assigned as developers and software architects throughout all project sprints, while we flipped the scrum master and product owner roles every two sprints. The scrum master is responsible for overseeing the sprint reports and meeting while the product owner makes sure that we are inline with the requirements and test cases of the system.

**In Sprint 1 & 2:**

-   Scrum master: Kanokwan
    
-   Product owner: Nazli.
    

**In Sprint 3 & 4:**

-   Scrum master: Cynthia
    
-   Product owner: Marwa.

## Links to all relevant related team resources (Trello board, source-code repositories etc.)

**Trello**

We used the trello board to manage our project. It is divided into four different boards; the product backlog, sprint backlog, doing and done.

[Trello board](https://trello.com/b/FrFZpB43/dit-356-2022-team-5)

**Brief reference to codes and commits, with a walkthrough to GitLab repos**

Dentistimo is a distributed system with a monolithic database that consists of 4 components that are connected through MQTT. Below is a detailed description of the components and their responsibilities:

  

 

 - **Booking handler:
   ([https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler))**

This component is responsible for checking if a timeslot selected by a user is available. Before approving a new booking, it double checks in the database the availability of selected date and time. When a booking is successful, it is stored in the database and an email confirmation to the user and the user receives an email confirming their appointment booking, to make this possible we use nodemailer. It is also responsible for getting specific users appointments as well as deleting them upon request.
This component communicates with the user interface and the bidirectional transfer of information happens through HIVEMQ
We used the opossum library for the circuit breaker. To test fault tolerance, we used a MQTT Box to perfom a load test where we sent 100 booking requests to the component.

**Important commits of this repository:**

Availability checker:

[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/1118c7d9cdc3d3905da221589bb7b52d01aaeac5](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/1118c7d9cdc3d3905da221589bb7b52d01aaeac5)

Approve booking: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/ab8d02b4a2ae8685105b7fbfb945e82366777000](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/ab8d02b4a2ae8685105b7fbfb945e82366777000)

Send booking confirmation email: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/0fb2a3eca1b8946b2629cabcd3aebc70b9cfb615](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/0fb2a3eca1b8946b2629cabcd3aebc70b9cfb615)

Receive the list of appointments:

[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/5c50341c6a843db16c5572706a3fb4e091deda9d](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/5c50341c6a843db16c5572706a3fb4e091deda9d)

Adding the circuit breaker:

[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/d9c86596f748403fdea8a1892a6c31cabd5c9e44](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/d9c86596f748403fdea8a1892a6c31cabd5c9e44)

Deleting the appointments:

[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/1b6d45de40964d195904f3aeec79a9176ef88b82](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/bookinghandler/-/commit/1b6d45de40964d195904f3aeec79a9176ef88b82)

  

 - **Dentist handler:
   ([https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-dentisthandler](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-dentisthandler))**

The dentist handler is responsible for fetching dentist data from the dentistry Json file using node fetch and saving it to mongoDB without duplicates. When it receives requests from the user interface to either get all dentists or get a specific dentist by id, it searches for it in the database and if successful, it sends back a response with the results. This bidirectional transfer of information happens through HIVEMQ

**Important commits for this component:**

Final commit of getting the dentists data and modification in the models: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-dentisthandler/-/commit/40716d189bf6419859ef6bf5bc1985ce545a3580](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-dentisthandler/-/commit/40716d189bf6419859ef6bf5bc1985ce545a3580)

  

Documentation: ([https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-documentation](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-documentation))

Documentation repository consists of the diagrams, SRS requirements, Description of architectural styles, Design decisions, Architecture drivers. There is a folder of diagrams such as ER diagram, functional decomposition diagram, and component diagram which display the workflow and idea behind each of the components in the Dentistimo distributed system.

  

 - **User handler: 
   ([https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler))**

The user handler is responsible for handling user information sent to it by the user interface component. It is responsible for creating a new user and when successful an email confirmation awaiting verification is sent to the user using nodemailer. When an existing user signs in, it handles the authentication by matching provided data with data saved in the database.Moreover, it is responsible for getting user’s information, editing user information. This component communicates with the user interface and the bidirectional transfer of information happens through HIVEMQ

**Important commits for this component:**

Sign in: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/b2d3783e3989c655326c4b6db03610d0d48c247c](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/b2d3783e3989c655326c4b6db03610d0d48c247c)

Sign up:  [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/ae743413ee277a394561fdb8c052705d6f0a3029](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/ae743413ee277a394561fdb8c052705d6f0a3029)

Email verification:

[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/9ba2cd4ee41a46c50597467b546a9327d83a0a8bUpdate profile](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/9ba2cd4ee41a46c50597467b546a9327d83a0a8bUpdate)

Profile page: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/29c91cb50cef9d2127993f03c6b03fc09c511d73](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userhandler/-/commit/29c91cb50cef9d2127993f03c6b03fc09c511d73)

  

 - **User interface: 
   ([https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface))**

User interface is the component which communicates with other 4 components through the mqtt broker.

This component enables the user to interact with the system via graphical user interface. We used NodeJS to create the website and VUE.js to design the interface. To display the dentist locations on a map, we used leaflet. The component utilizes the Vuex library to create a session for the logged in user.

  

We used a websocket to ensure a two-way interactive communication session between the user's browser and a server. The user can sign up, sign in, update their information, see upcoming appointments as well as cancel on the profile page, see dentist locations displayed on a map, they can pick a clinic, see the available time slots, and finally pick a date and time to book an appointment.

  

**Important commits for this component:**

Booking, dentist list, time : [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/1bed22240655bf0327489eccefa972ce878a8b7e](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/1bed22240655bf0327489eccefa972ce878a8b7e)

Delete appointment frontend: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/3261ea1051c5857266ff91bdfc1d5d4f85eead4b](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/3261ea1051c5857266ff91bdfc1d5d4f85eead4b)

Final availability checker(updated one) and some changes in the css of navbar :[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/a316da1f53eac24e979f1f30aec807bc6cdcff7f](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/a316da1f53eac24e979f1f30aec807bc6cdcff7f)

Update profile frontend implementation: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/5dbf92bb335d65cce7e78ae301ad1df156fa732d](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/5dbf92bb335d65cce7e78ae301ad1df156fa732d)

Creating a session for logged in user: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/37f10abb2be24d5eae15fd5a3f2385bfca6a836f](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/37f10abb2be24d5eae15fd5a3f2385bfca6a836f)

Login with mqtt connection: [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/7665b9cbfee64e367541dc0bafa5178a586df2b3](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/7665b9cbfee64e367541dc0bafa5178a586df2b3)

Sign up with mqtt connection :[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/ae30e09eab06911fe3a7b3226e30a8bd8b753e02](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/ae30e09eab06911fe3a7b3226e30a8bd8b753e02)

[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/440887b036f69cbb4d52db6942cddeef8ca87ef8](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/440887b036f69cbb4d52db6942cddeef8ca87ef8)

Mqtt dentist mapping : [https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/ed92f2d78f8e3176cfb70702d9246495ef4f71bf](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/ed92f2d78f8e3176cfb70702d9246495ef4f71bf)

Final timeslot changes with booking:

[https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/e70937ce10fcb307bc91c4ca54700c990bb6081d](https://git.chalmers.se/courses/dit355/dit356-2022/t-5/t-5-userinterface/-/commit/e70937ce10fcb307bc91c4ca54700c990bb6081d)