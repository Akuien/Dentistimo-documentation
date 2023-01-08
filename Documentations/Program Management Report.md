# Sprint Reports
All of this can be seen on Trello : [https://trello.com/b/FrFZpB43/dit-356-2022-team-5](https://trello.com/b/FrFZpB43/dit-356-2022-team-5)
## SPRINT 1 REPORT
|  start| end |
|--|-- |
 | 7/11/2022 |18/11/2022 |
The sprint is planned to be two weeks long. After each week, we will have a weekly update to see the progress before going to the next week. We also plan on having daily scrum meetings at 18:00 to check on individual progress and possible challenges on days that we do not have team meetings.
 
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
 
The sprint is planned to be two weeks long. After each week, we will have a weekly update to see the progress before going to the next week. We also plan on having daily scrum meetings at 17:30 to check on individual progress and possible challenges on days that we do not have team meetings.
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
The sprint is planned to be two weeks long. After each week, we will have a weekly update to see the progress before going to the next week. We also plan on having daily scrum meetings at 17:30 to check on individual progress and possible challenges on days that we do not have team meetings.
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


The sprint is planned to be two weeks long. After each week, we will have a weekly update to see the progress before going to the next week. We also plan on having daily scrum meetings at 17:30 to check on individual progress and possible challenges on days that we do not have team meetings.
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