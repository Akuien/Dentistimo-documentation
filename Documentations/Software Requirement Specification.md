# Software Requirement Specification (SRS)

## Functional Requirements (FR)
<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>Functional Requirement Description</th>
            <th>User Story(s)</th>
            <th>Acceptance criteria</th>
        </tr>
    </thead>
    <tbody>
     <td>FR1</td>
            <td>The system shall be divided into 5 sub-systems.</td>
            </tr>
            <tr>
            <td>FR2</td>
            <td>The system shall use middleware based on the MQTT-protocol.
</td>
            </tr>
            <tr>
            <td>FR3</td>
            <td>The system shall use publish-subscribe architecture.</td>
            </tr>
            <tr>
            <td>FR4</td>
            <td>The system shall use pipe and filter architecture.</td>
            </tr>
        <tr>
            <td>FR5</td>
            <td>The system shall allow the creation of new users.</td>
            <td>
                <ul>
                    <li>
                        As a user I want to be able to create an account using the Destistimo system so that I can     be able to login and book an appointment with my dentist and log out as well.
                    </li>
                </ul>
            </td>
            <td>
            <ul>
            <li>
            A user cannot submit a form without completing all the mandatory fields.
            </li>
            <li>
            Information from the registration form should be saved in the mongoDB.
            </li>
            </ul>
            </td>
        </tr>
        <tr>
            <td>FR6</td>
            <td>The system shall allow a registered user to login and logout.</td>
            <td>
                <ul>
                    <li>
                        As a user, I want to be able to login to the system. so that I can book an appointment.
                    </li>
                </ul>
            </td>
            <td>
            <ul>
            <li> A user cannot submit a form without completing all the mandatory fields.</li>
            </ul>
              <ul>
            <li>Validated users should be directed to the home page.</li>
            </ul>
             <ul>
            <li>The user’s credentials should be saved in the local storage.</li>
            </ul>
            </td>
        </tr>
         <tr>
            <td>FR7</td>
            <td>The system shall display Gothenburg dentists offices on a map.</td>
            <td>
                <ul>
                    <li>
                        As a user who requires dental care, I want to see where the dental clinics are located on  a map, so that I can see which clinic is the closest to me.
                    </li>
                </ul>
            </td>
            <td>
            <ul>
            <li>There should be markers on the map to display the location of the clinics.</li>
            </ul>
            </td>
        </tr>
         <tr>
            <td>FR8</td>
            <td>The system shall allow users to see the information of dental clinics alongside with their location on the map. </td>
            <td>
                <ul>
                    <li>
                        As a user, I want to be able to navigate on the map, so that I can see the dentist offices, and see the related information about a specific clinic.
                    </li>
                </ul>
                 <td>
                <ul>
                    <li>
                        The information about each of the clinics should be displayed next to the map.
                    </li>
                </ul>
                 </ul>
             <ul>
            <li>The size of the marker of the specific location should be maximized while the user hovers over the box of the clinic’s information.</li>
            </ul>
            </td> 
            </td>
        </tr>
         <tr>
            <td>FR9</td>
            <td>The system shall allow users to view available time slots.
            The appointments are 30 minutes long
            The dentist has 1 hour lunch break and 30 minutes Fika break.
            </td>
            <td>
                <ul>
                    <li>
                     As a user, I want to be able to see all the available time slots from the dental clinic of my choice, so that I can see which available time suits me the best.
                    </li>
                </ul>
            </td>
            <td>
                <ul>
                    <li>
                       The available time slots should be displayed in the booking page.
                    </li>
                </ul>
                 </ul>
            </td> 
        </tr>
         <tr>
            <td>FR10</td>
            <td>The system shall allow the user to book an appoitment from the selected available timeslot.</td>
            <td>
                <ul>
                    <li>
                      As a user, I want to book an appointment at a certain dental clinic which I think is the best based on the availability of the timeslot and location.
                    </li>
                </ul>
            </td>
            <td>
                <ul>
                    <li>
                       The user should be able to click a button to check the availability of the timeslot
                    </li>
                </ul>
                <ul>
                    <li>
                       The user should be able to click a button to check the availability of the timeslot
                    </li>
                </ul>
                <ul>
                    <li>
                       The user should be able to click a button to book an available timeslot. 
                    </li>
                </ul>
                <ul>
                    <li>
                       The booking should be saved to the database. 
                    </li>
                </ul>
                 </ul>
            </td> 
        </tr>
         <tr>
            <td>FR11</td>
            <td>The system shall send a confirmation message to the user when an appointment is successfully booked.
</td>
            <td>
                <ul>
                    <li>
                    As a user I want to be able to get an email notification and message after successfully booking an appointment, so that I know my appointment is being made.
                    </li>
                </ul>
            </td>
            <td>
                <ul>
                    <li>
                       A message that confirms that the booking was successful is shown on the screen.
                    </li>
                </ul>
                <ul>
                    <li>
                       A booking confirmation email is sent out to the user.
                    </li>
                </ul>
                </td>
        </tr>
         <tr>
            <td>FR12</td>
            <td>The system shall send a rejection message to the user when an appointment booking attempt is unsuccessful.</td>
            <td>
                <ul>
                    <li>
                    As a user I want to be notified when my booking was unsuccessful, so I can try again.
                    </li>
                </ul>
            </td>
            <td>
            <ul>
                    <li>
                      A message that informs the user that the booking was unsuccessful is shown on the screen
                    </li>
                </ul>
                </td>
            <td>FR13</td>
            <td>The system should allow users to view their upcoming appointmets.</td>
            <td>
                <ul>
                    <li>
                        As a user, I want to view my upcoming appointments, so that I can keep track of all my appointments.
                    </li>
                </ul>
            </td>
            <td>
            <ul>
                    <li>
                        A list of a user’s upcoming appointments should be available when logged in to the system.
                    </li>
                </ul>
                <ul>
                    <li>
                       The list should contain information about date and time for each appointment.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR14</td>
            <td>The system should allow users to edit and update their information.
</td>
            <td>
                <ul>
                    <li>
                        As a user, I want to change my information in the system, so I can keep my account up to date.  
                    </li>
                </ul>
            </td>
            <td>
            <ul>
                    <li>
                        A user should be able to fill out a form to update their information.
                    </li>
                </ul>
                <ul>
                    <li>
                        New user information should be saved to the database.
                    </li>
                </ul>
            </td>
        </tr>
        <tr>
        <td>FR15</td>
            <td>The system shall allow the user to cancel their appointments.</td>
            <td>
                <ul>
                    <li>
                        As a user who is not available for the scheduled appointment, I want to cancel my appointment, so I can go through the booking process any other time.   
                    </li>
                </ul>
            </td>
            <td>
            <ul>
                    <li>
                        Canceled appointments should be removed from the users upcoming appointments.
                    </li>
                </ul>
                <ul>
                    <li>
                        Canceled appointments should be made available in the database for other users to book.
                    </li>
                </ul>
            </td>
        </tr>
        <tr>
        <td>FR16</td>
            <td>The system shall send a confirmation email to the user after creating an account.</td>
             <td>
                <ul>
                    <li>
                        As a user I want to make sure that the account that I created has been registered to the system.      
                    </li>
                </ul>
            </td>
            <td>
            <ul>
                    <li>
                        A confirmation email should be sent to the email address of the registered user.
                    </li>
                </ul>
            </td>
            </tr>
            <tr>

    </tbody>
</table>

## Non-Functional Requirements (NFR)
 
 1. Usability
  1.1 The system must be easy to use. 98% of users should be able to use the system without confusion.
  1.2 95% of users shall be able to book an appointment in one minute.
  1.3 The error rate of users booking an appointment must not exceed 5 percent.

 2. Security 
  2.1 User information such as passwords should be kept confidential and secure by the system.

 3. Portability
  3.1 The system should be able to run on all device platforms without any change in its behaviour and performance.

 4. Scalability
The system must be able to support many user visits at the same time while maintaining optimal performance.

## Constraints

1. The system should follow GDPR guidelines.
2. The system shall be a distributed system consisting of at least 4 components.
3. The system shall use a MQTT broker to for communication between the component
