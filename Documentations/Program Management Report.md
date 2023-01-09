# Sprint Reports
All of this can be seen on Trello : [https://trello.com/b/FrFZpB43/dit-356-2022-team-5](https://trello.com/b/FrFZpB43/dit-356-2022-team-5)
Each sprint is planned to be two weeks long. After every week, we will have a weekly update to see the progress before going to the next week. We also plan on having daily scrum meetings at 18:00 to check on individual progress and possible challenges on days that we do not have team meetings.

## SPRINT 1 REPORT
|  start| end |
|--|-- |
 | 7/11/2022 |18/11/2022 |


 
| Tasks                                    | Priority | Task Description                                                                                        | Estimated hours |
|------------------------------------------|----------|---------------------------------------------------------------------------------------------------------|-----------------|
| ER Diagram                               | Medium   | Draw Entity diagram to show the system's entities like user, appointment and how they interact.         | 3               |
| Functional Decomposition Diagram         | Medium   | Draw the functional decomposition diagram to show the breakdown of the system based on functionalities. | 2               |
| Architectural Styles Diagram             | High     | Choose the architectural style and draw a  diagram to illustrate it                                     | 3               |
| Component Diagram                        | Low      | Draw a components diagram to show the system breakdown based on the components                          | 3               |
| SRS Requirement                          | High     | Come up and document systems requirement                                                                | 4               |
| User Stories                             | High     | Brainstorm and come up with user stories of what the system should do                                   | 5               |
| Sitemap                                  | Low      | Draw a diagram to elaborate how different pages of the web frontend/UI interacts                        | 3               |
| Screen Planning                          | Low      | Design the screen pages using figma                                                                     | 6               |
| Schema Planning                          | Medium   | Research and come up with how the schemas should be implemented                                         | 1               |
| Architectural Styles Planning            | High     | Plan on how to actualize the chosen architecture style                                                  | 1               |
| Project Proposal                         | Medium   | Document the project proposal/vision/chart                                                              | 2               |
| Map screen                               | Medium   | research on adding the map to show the dentists’ location in the system                                 | 3               |
| MQTT connection                          | Medium   | Research on how to add, implement and use mqtt                                                          | 3               |
| Schema and db connection                 | Medium   | Set up mongoDB database and the schemas                                                                 | 2               |
| Authentication jwt and user for security | Medium   | Work on using encrypting and decrypting users password before adding to the database                    | 5               |
| Set up CI/CD pipelines                   | Medium   | Set up the CI pipeline for code quality                                                                 | 2               |
| Retrospective 1                          | Medium   | Complete the retrospective on our progress                                                              | 3               |

 **1. What went well**

> -   we managed to finish most of the sprint backlog
>     
> -   work well as a team, no conflict yet
>     
> -   the meetings we had were productive

 **2. What can be improved both in working process and code**

> -   The navigation between the screens(code)
>     
> -   practicing scrum correctly(process)
>     
> -   Understanding and learning more how MQTT works and connects the components together. (code)

**3. Velocity**
![1](https://media.discordapp.net/attachments/1061775332039987241/1061784464520396860/1.jpg)

## SPRINT 2 REPORT
|  start| end |
|--|-- |
 | 21/11/2022 |2/12/2022 |
 


|                      Tasks                      | Priority |                                       Description                                      | Estimated hours |
|-----------------------------------------------|:--------:|--------------------------------------------------------------------------------------|:---------------:|
| Sprint 2 planning                               |   High   | Plan and document sprint 2                                                             |        2        |
| MQTT connection                                 |   High   | Set up mqtt and connect some components                                                |        4        |
| Generate time slots for appointments            |  Medium  | Research and implement the timeslot generator slots to generate timeslots to be booked |        4        |
| Availability checkers                           |  Medium  | Add availability checker to check be use to check available time slots                 |        4        |
| User Handler                                    |  Medium  | Add user handler component to handler authentication and registration                  |        5        |
| Email Verification                              |  Medium  | Enable the system to send verification email after user registration                   |        3        |
| Hiding information in environment variable file |  Medium  | Add .env file to hide mongoDB and mqtt cluster sensitive credentials                   |        1        |
| Email verification when user signs up           |  Medium  | Enable the system to send verification email after user registration                   |        3        |
| Add clinics locations to map                    |  Medium  | Enable the screen to show the location of a clinic on the map page                     |        2        |
| Save dentists to db                             |    Low   | Fetch and save the dentist details in db                                               |        1        |
| Retrospective 2                                 |  Medium  | Complete and submit retrospective 2 to show our project progress                       |        3        |
| TA sessions                                     |  Medium  | Communicate, plan and attend sessions                                                  |      20mins     |
| Daily Scrums                                    |  Medium  | Plan and attend all daily scrums for team updates                                      |      15mins     |
| Avoid dentist data duplication                  | Low      | Fix bug which duplicates dentist data                                                  | 2               |
| Display calendar                                | Medium   | Add calendar on the frontend                                                           | 4               |

 **1. What went well**

> -   Email verification
>     
> -   Saving dentists to db using node fetch


 **2. What can be improved both in working process and code**

> -   improve communication and meetings
>     
> -   Better Organization of task since we realized many tasks and components are dependent on others

**3. Velocity**
![2](https://cdn.discordapp.com/attachments/1061775332039987241/1061784464713330739/2.jpg)
## SPRINT 3 REPORT
|  start| end |
|--|-- |
 | 5/12/2022 |16/12/2022 |
 


|                      Tasks                      | Priority |                               Description                               | Estimated hours |
|-----------------------------------------------|:--------:|-----------------------------------------------------------------------|:---------------:|
| Sprint 3 planning                               | High     | Plan and document sprint 3                                              | 1h              |
| **Week 1**                                          |          |                                                                         |                 |
| change login from api to mqtt                   | Medium   | Use mqtt to implement the login process of a user                       | 10h             |
| change signup from api to mqtt                  | Medium   | Use mqtt broker to implement registration of a user                     | 9h              |
| display user profile                            | Low      | Create a page to display user info/profile                              | 10h             |
| display upcoming appointments                   | Medium   | Implement a feature to enable user to see their upcoming appointments   | 5h              |
| Display dentists in map                         | High     | Display dentist/click location on the map page                          | 15h             |
| Display dentist information e.g opening hours   | High     | Implement the display of dentist opening and closing hours              | 3h              |
| Select a dentist by ID                          | High     | Implement selecting a dentist using their ID                            | 8h              |
| Retrospective 3                                 | Medium   | Complete and submit retrospective 3 to show our progress                | 4h              |
| **Week 2**                                          |          |                                                                         |                 |
| generate time slots of selected dentist clinic  | High     | Implement generation of timeslots of a specific selected dentist clinic | 8h              |
| Add web sockets to user interface               | High     | Enable websocket connection on the web client browser                   | 5h              |
| Create session for logged in user               | Medium   | Implement a session to enable tracking of a logged in user              | 3h              |
| Update documentation                            | Low      | Update readMe and project documentation                                 | 10h             |
| Update readme files                             | Medium   | Update Gitlab readMe                                                    | 5h              |
| Accept booking and save to mongodb              | Medium   | Implement acceptance of a booking and save it to db                     | 5h              |
| Sprint 3 review                                 | Medium   | Do and document sprint review                                           | 1h              |

**1. What went well**

> -   Web sockets works
>     
> -   Map and map markers with dentists info
>     
> -   Sign up and login
>     
> -   Create a session for the logged in user
>     
> -   Updated all readme files and team documentations.
>     
> -   appointments timeslots
>     
> -   We have a better understanding of mqtt
> 
**2. What can be improved both in working process and code**
> -   Better prioritization of tasks
>     
> -   Keep track of how many hours a person worked on a task so that we can compare with the estimated time.

**3. Velocity**
![3](https://cdn.discordapp.com/attachments/1061775332039987241/1061784464918839296/3.jpg)
## SPRINT 4 REPORT

|  start| end |
|--|-- |
 | 19/12/2022 |30/12/2022 |



|                             Tasks                             | Priority  | Estimated time | Actual time |
|-------------------------------------------------------------|:---------:|:--------------:|:-----------:|
|                       Sprint 4 planning                       |    High   |       1h       |     30m     |
|                             **Week 1**                            |           |                |             |
|                      display user profile                     |    High   |       10h      |     11h     |
|                     User can edit profile                     |   Medium  |       5h       |      8h     |
|                 display upcoming appointments                 |   Medium  |       5h       |      5h     |
|                      Cancel appointments                      |    High   |       3h       |      5h     |
|                     confirm/reject booking                    |    High   |       6h       |      8h     |
|              display time slots on user interface             |    High   |       9h       |     10h     |
| show appointment confirmation/rejection message after booking |   Medium  |       3h       |      3h     |
|                             **Week 2**                            |           |                |             |
|                show availability on chosen date               |   Medium  |       3h       |      5h     |
|            Add circuit breaker to booking component           |   Medium  |       1h       |      2h     |
| Retrospective 4                                               | High      | 3h             | 4h          |
| Project brief                                                 | High      | 9h             | 9h          |
| Send multiple booking requests using MQTTBox                  | High      | 6h             | 8h          |
| Sprint 4 PMR                                                  | Medium    | 1h             | 1h          |


**1. What went well**

> - Done with most of the requirements of the system

**2. What can be improved both in working process and code**

> -   Appointment shows its deleted only when page is automatically refreshed
>     
>     
> -   Keep session of logged in user alive
>     


**3. Velocity**
![4](https://cdn.discordapp.com/attachments/1061775332039987241/1061784465187291236/4.jpg)

## **Weekly Update**


| Week   | Update                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Week 1 | This week was mostly used for project planning, selecting the key functionality,  system components and its architectural styles. The Functional decomposition diagram, ER diagram, and component diagram are the main methods we select to implement for system’s planning. Scrum master(Kanokwan Haesatith ) Product Owner( Nazli Moghaddam)                                                                                                                                                                                                                                                                                                                                                                                                              |
| Week 2 | The tasks in this week were assignable so we went on to start assigning different tasks to team members and also planning poker time estimation for each task.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Week 3 | This week, we decided to adjust the daily scrums meeting time from 18:00 to 17:30 as many team members find starting the meeting earlier is more productive for us as a group and sprint planning for sprint 2.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Week 4 | we have difficulties with implementing the map with mapbox so we decide to switch to leaflet api instead. Geojson is a worldwide json format specifically used in all apps like google maps or apple map. But the data that we have on github( provided by the teacher) is in normal json format not geojson so we didn’t use the geojson format to map the location. Just normal json Started having 2 long meetings (Monday, Wednesday)every week instead of one as we thought it was more efficient and gives us more time to have longer discussions and get team work done. We decided to switch login from api to mqtt implementation of login/signup process of a user, due to difficulties faced with api and communication between ui/userhandler. |
| Week 5 | When the user signs up the password is encrypted. In this case the new user is not able to login with the credentials they have, so we have to decide how to implement that part to enable the user to login without any difficulties. Due to lack of resources, we decided to switch to using leaflet api for mapping dentists instead of mapbox that we deemed more difficult. Scrum master(Cynthia Tarwireyi ) Product Owner(Marwa Selwaye ) pair programming: At the end of week 5 we decided to change our working techniques due to inefficiency in work progress, so  we decided on doing pair programming where we would work in pairs on certain areas of the project.                                                                             |
| Week 6 | We had some issues concerning mqtt connection so we decided to take some time to work on fixing that and understanding it more individually. A member of our team left the course in the beginning of this sprint so we became 6 members in the team                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Week 7 | No major changes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Week 8 | Timeslots change: We are not using the generated time slots from the timeslot generator component anymore, and using hard coded time slots instead where the user can select based on the opening times of each clinic, and be prevented from making an appointment out of the opening and closing times. The reason for the change was that there were bugs on the front end that caused some issues.  Moved availability checker from the timeslots generator component to booking handler.                                                                                                                                                                                                                                                               |

## Project management practices used during the development process

To make our project consistent with agile practices, we tried to follow all the agile project management practices and phases. These practices and phases were done and implemented over the different sprints we had during the development of the project starting from sprint one to four. These phases involved project planning, elaboration and project construction/implementation phase. All are elaborated and described further below. 

**1.  Project planning/Inception phase**
    

During this part of the agile practice, we took time to make plans on the project; the tools and technologies we were going to use, the communication means, assigning team members with different roles and responsibilities and also decisions concerning the project implementation.

To actualize these things, we drew a [team contract and agreement](https://docs.google.com/document/d/1TV__3F4iAxFeXiiyypLPCVCRJQ910vjezVbvgp2Kr5g/edit) to act as a point of reference as we worked on the project later on. We also set up the tools and technologies decided upon and lastly documented the [project proposal](https://docs.google.com/document/d/1bKyFMJI-BU9DHj2VMGdoc-TIq0MAsdkRlbpeAhV9xq4/edit) based on the description and requirements provided by the product owner.

Since transparency is one of the most significant characteristics that makes project agile teams perform better, we put that into consideration when planning for the project. We considered multiple factors that could lead to a better transparency for all team members, like getting notified on every change on the trello board, on gitlab repos, our docs are shared and include all latest updates on each task in every sprint backlog. Those actions helped all team members be on the same page of how the project is processing and have visibility into the big picture of the project.

  

**2.  Project elaboration phase**
    

This phase mostly involved the designing and modeling of the proposed system. We came up with the [system requirements](https://docs.google.com/document/d/1jOVEwfz0SPGKZOQC_dQp3wa6PZpzPpl_1GxAO7iYuqo/edit) of the system, architectural requirements, [user stories](https://docs.google.com/document/d/1FKB84jf6prODfqYHYSRRvSg3nYoLjHFpjEFsFCoNhfg/edit), architecture choice, design and justification, system functional decomposition diagram, the components diagram and the system architecture diagram.

*User stories:*
For agile development, we came up with the systems’ user stories based on the systems’ requirements we gathered. These user stories helped us the developers to understand the system, develop the system iteratively and incrementally and also in a coherent and consistent way. The user stories we uniquely number ID and tasks were created out of them and added to the product backlog helping in our scrum process.

  
  

**3.  Project Construction/Agile development**
    
On this part of the project, in order to adhere with agile best practices for the project management, we used scrum methodology with four sprints each led by sprint planning, sprint review and retrospective to help us monitor and control the project all through the process of implementation and also keep track on all decisions made on the progress, the project, the scope and the requirements.

  

*Sprint planning*

> To keep track of the progress, fulfill an iterative development of the
> project we had sprint plannings at the beginning of each sprint to
> assign the tasks to members and keep track of what was being done and
> delivered. Each sprint was two weeks long accompanied by the daily
> scrum stand up meetings and weekly update of deliverables and tasks.

  

*Continuous Integration and Delivery*

> CI/CD automates the building and testing of our software and by the
> continuous deployment which is an extension of this automation, it
> allows our system to be deployed after every code commit that has
> passed our tests and helped us ensure the quality of the code and
> minimize the risk of errors.
> 
> Stages used in our components pipelines: Build stage: which includes
> compile code and docker build phases. Build stage automates developer
> contributions and provides tools to standardize our software quality
> and environments.

  

*Incremental delivery*

> Each sprint we used our user stories and requirements as guidelines
> for what we wanted to implement during the upcoming sprint. We chose
> our most important user stories and made them into tasks. Bigger tasks
> were divided into subtasks which we wrote as a checklist on our Trello
> board cards to easier keep track of what needed to be implemented, and
> the tasks were later assigned to different team members. We planned
> for each feature to be delivered and integrated into the system at the
> latest at the end of the sprint. However, most of the time we had to
> prioritize certain tasks and deliver them as fast as possible to avoid
> problems with dependencies between different tasks.

  
  

*Project Documentation*

> For the project documentation, we had a project google drive where all
> the meetings, plans and decisions of the project were recorded and
> kept and accessed by all team members. All tasks and practices were
> recorded ranging from the team agreement, sprint plans and
> reviews/retrospective and weekly updates.
> 
> We applied an agile approach in documenting tasks status through;
> Continuous result delivery  updates  and sharing tasks status and
> insights with the team to ensure consistent continuous feedback and
> allowing for problems to be sifted out as soon as they arise. The
> assessment of the project’s progress against the project plan, and if
> the project is ahead or behind schedule and that is done by ensuring
> the proper documentation of each task status in each sprint report,
> and adding key informations, such as:
> 
> -   Works that has been completed (status: done/undone)
>     
> -   Estimated time for completion and actual time it takes to complete
>     
> -   Priority for each task(High, medium, low)

    

  
  

*Understanding all risks ( Risk Analysis )*

> To prepare for the unknown and help us monitor and control hence
> manage the project well, we consistently carried out our risk analysis
> to identify potential risks like falling behind the schedule ,
> spending too much time on a challenge and team members falling behind
> or sick and unable to do their tasks. This helped us ensure delivery
> on time.
