# Software Requirement Specification (SRS)

## Functional Requirements (FR)
<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>Functional Requirement Description</th>
            <th>User Story(s)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>FR1</td>
            <td>The system shall allow the creation of new users.</td>
            <td>
                <ul>
                    <li>
                        As a user I want to be able to create an account using the destistimo system so that I can be able to login and book an appointment with my dentist and log out as well.
                    </li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>FR2</td>
            <td>The system shall allow a registered user to login and logout.</td>
            <td>
                <ul>
                    <li>
                        As a user, i want to be able to login to the system. so that i can book a dental appointment.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR3</td>
            <td>The system shall display Gothenburg dentists offices on a map.</td>
            <td>
                <ul>
                    <li>
                        As a user who requires dental care, I want to see where the dental clinics are located on a map, so that I can see which one is the closest to me.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR4</td>
            <td>The system shall allow users to select a dentistry on the map.</td>
            <td>
                <ul>
                    <li>
                        As a user, i want to be able to navigate on the map, so that i can select the dentist office i want to visit.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR5</td>
            <td>The system shall provide information about the dentist office selected by the user.</td>
            <td>
                <ul>
                    <li>
                    As a user I want to be able to see the information and details of any dentist office I select so that I can make my decision from there before booking or not on whether it fits me best or not.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR6</td>
            <td>The system should allow users to view available time slots.</td>
            <td>
                <ul>
                    <li>
                      As a user, I want to be able to see all the available time slots from the dental clinic of my choice, so that I can see which available time suits me best.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR7</td>
            <td>The system shall allow the user to book an appoitment from the selected available timeslot.</td>
            <td>
                <ul>
                    <li>
                       As a user, I want to book an appointment at a certain dental clinic, so that I can have my dental needs attended to.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR8</td>
            <td>The system shall provide information about the dentist office selected by the user.</td>
            <td>
                <ul>
                    <li>
                        As a user who wants to view available dentists, I want to see a list of dentists with their key information, so that I can have a full view of dentists.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR9</td>
            <td>The system shall allow the user to cancel their appointment up to 24 before the appointment.</td>
            <td>
                <ul>
                    <li>
                    As a user who is not available for my scheduled appointment, I want to cancel my appointment, so that I do not have to pay a no show up fee.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR10</td>
            <td>The system shall send the user a reminder email 48 hours before their appointment. </td>
            <td>
                <ul>
                    <li>
                       As a user, I want to get a email notification about my booked appointment 24 hours before the appointment time, so that I do not forget to show up.
                    </li>
                </ul>
            </td>
        </tr>
         <tr>
            <td>FR11</td>
            <td>The system shall send a confirmation message to the user when an appointment is successfully booked.</td>
            <td>
                <ul>
                    <li>
                    As a user I want to be able to get a notification after successfully booking an appointment, so that I know my appointment is set.
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
                    As a user I want to be notifed when my booking was unsuccessful, so that I can rebook.
                    </li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>FR13</td>
            <td>The system shall ​​allow users to get directions to their appointment through Google Maps.</td>
            <td>
                <ul>
                    <li>
                        As a user who has an upcoming appointment, I want to get directions to the dentist clinic, so that I can easily navigate to my appointment.
                    </li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>FR14</td>
            <td>TThe system should allow users to view their upcoming appointmets.</td>
            <td>
                <ul>
                    <li>
                        As a user, I want to view my upcoming appointments, so that I can keep track of all my appointments.
                    </li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Non-Functional Requirements (NFR)
 
 1. Usability
  1.1 The system must be easy to use. 98% of users should be able to use the system with ease.
  1.2 95% of users shall be able to book an appointment in one minute.
  1.3 The error rate of users booking an appointment must not exceed 5 percent.

 2. Security 
  2.1 The system shall keep the users information confidential and secure

 3. Portability
  3.1 The system should be able to run on all device platforms without any change in its behaviour and performance.

 4. Scalability
The system must be able to support many user visits at the same time while maintaining optimal performance.

## Constraints

1. The system should follow GDPR guidelines.
2. The system shall be a distributed system consisting of at least 4 components.
3. The system shall use a MQTT broker to for communication between the component
