# EventShare Web App

EventShare is a web application designed to streamline event management and discovery within Northeastern University. This platform allows users to explore, share, and engage with various events on campus. Whether you're a student, faculty member, or staff, EventShare has features tailored to enhance your event experience.
## Features
### User Features
#### 1 View All Events
Search and view through a comprehensive list of all upcoming events at Northeastern University.
#### 2 View on Maps
Visualize event locations on an interactive map for better navigation.
#### 3 Share Event
Easily share events with friends and colleagues through various social media platforms or email.
#### 4 Buy Tickets
Purchase tickets for events directly through the app for a seamless experience.
#### 5 Rate Events
Provide feedback on events by rating them, contributing to a dynamic and user-driven event community.
#### 6 Add to Favorites
Save your favorite events for quick access and personalized event recommendations.

## Admin Features
### CRUD Operations
#### Perform Create, Read, Update, and Delete operations for events to manage and curate the event calendar.

### Admin Screen
Admin wil be able to manage the events (CRUD operation)

- **Create Event:**
  Admin has the rights to create a new event and enter the details of the event

- **View Event:**
  Admin can view the event and see its details

- **Update Event:**
  Admin can update an event to change any specific details related to an event, like change in time, location, date, etc.

- **Delete Event:**
  Admin can delete an event if a event has been cancelled or it no longer exists.


## Technical Features
### 1) Internationalization (i18n)
Support for English and French languages to cater to a diverse user base.
### 2) Redux Integration
Utilize Redux for state management, ensuring a scalable and maintainable application architecture.
### 3) Progressive Web App (PWA)
Enjoy a responsive and reliable experience with PWA capabilities, allowing users to access the app even when offline.
### 4) Responsive Design
A user-friendly interface that adapts seamlessly to various screen sizes and devices.
### 5) Secure Access
Accessible only by Northeastern University credentials, ensuring the safety and privacy of user data.
### 6) React Router DOM and Page Not Found
EventShare uses react-router-dom for client-side routing. If a user navigates to a non-existent route, they will be redirected to a "Page Not Found" component. The routing configuration can be found in the src/App.js file.

# Getting Started

```
git clone https://github.com/your-username/eventshare.git

```
# Install dependencies:

```
cd eventshare
npm install

```
# Configure environment variables:

## Set up environment variables for authentication and other sensitive information.
```
npm start

```
## Open your browser and navigate to http://localhost:3000 to access EventShare locally.


## Scheme for Event Table
Event_Name (String, required)     : Name of the event.

Target_Audience (String, required): Type of Audience.

Date (String, required)           : Date of the event (YYYY-MM-DD).

Event_Start_Time (String)         : Start Time of the event (HH:mm).

Event_End_Time (String)           : End Time of the event (HH:mm).

Location (String)                 : Location where the event will take place.

Description (String)              : Description about the event

Category (String)                 : Event Category

Organizer (String)                : Event Organizers

Event_Link (String)               : Registration Link

Price (string)                    : Event ticket Price

## Structure
The project is structured into the following layers:

Controller Layer: Handles incoming HTTP requests, processes them, and returns appropriate responses. Controllers are responsible for routing and request handling.

Service Layer: Contains business logic and acts as an intermediary between the controllers and the models. It handles the core functionality of the application, such as processing data and interacting with the database.

Models Layer: Defines the data structure and schema for events. In this case, the Event model consists of fields like EventName, Target_Audience, Date, Event_startTime, Event_endTime, and location.


## API Endpoints
The API provides the following endpoints to interact with events:

GET /events: Retrieve a list of all events.

GET /events/:id: Retrieve details of a specific event.

POST /events: Create a new event.

PUT /events/:id: Update details of a specific event.

DELETE /events/:id: Delete a specific event.


## API Examples
#### 1. Get All Events
Endpoint: GET /events

Description: Get a list of all events in the university

Response: (example in json format)

          [
            {
              "EventName": "Example Event",
              "Targer_audience": "UnderGrad Students",
              "Location": "MaEll Hall Auditorium",
              "Date": "2023-12-01",
              "Start_Time": "18:00"
              "End_Time": "18:00"
            },
            // ... other events
          ]

#### 2. Get Event by ID
Endpoint: GET /events/:id

Description: Get details of a specific event by its ID.

Response: (example in json format)

            {
              "EventName": "Diwali Celebration",
              "Targer_audience": "All",
              "Location": "Ell Hall Auditorium",
              "Date": "2023-12-01",
              "Start_Time": "15:00"
              "End_Time": "20:00"
            },

#### 3. Create New Event
Endpoint: POST /events

Description: Create a new event.

Request: (example in json format)

          {
              "EventName": "Thanks Giving",
              "Targer_audience": "All",
              "Location": "Curry Centre",
              "Date": "2023-12-01",
              "Start_Time": "17:00"
              "End_Time": "20:00"
            },

#### 4. Update Event
Endpoint: PUT /events/:id

Description: Update details of a specific event by its ID.

Request: (example in json format)

          {
              "EventName": "Thanks Giving",
              "Targer_audience": "All",
              "Location": "Snell Engg.",
              "Date": "2023-12-01",
              "Start_Time": "17:00"
              "End_Time": "20:00"
            },

#### 5. Delete Event
Endpoint: DELETE /events/:id

Description: Delete a specific event by its ID.

Response:

          {
            "message": "Event deleted successfully."
          }





## Object Model Diagram

![Alt Assignment 8 page design](/images/ObjectModelDiagram.png)

### Google Maps Integration:

The website leverages the Google Maps API to provide a dynamic map view for users.
Real-time location tracking allows users to visualize event venues, enhancing their understanding of event locations.


### User-Friendly Interface:

User-friendly design for the frontend, ensuring a positive experience for Users.
Events are presented in an organized manner, allowing Users to quickly find relevant information.

### Real-Time Location Tracking:

Integration of Google Maps API for dynamic event location representation.
Users can track event locations in real-time, enhancing their ability to attend events with ease.

## Technical Stack:

### Backend: 

Node.js (Express), MongoDB for database storage.

### Frontend: 

Next.js for dynamic and HTML, SCSS, Javascript for responsive UI.

### Maps Integration: 

Google Maps API for real-time location tracking.

### Authentication: 

Secure login system for Admin and User access using Northeastern credentials.
