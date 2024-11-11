# CalendarAppDevelopment
Calendar App

A simple calendar application that allows users to schedule and manage events. This project demonstrates basic CRUD functionality, a user-friendly calendar interface, browser notifications, and additional features for searching and filtering events.
Table of Contents

    Project Structure
    Technologies Used
    Features
    Setup Instructions
    Usage
    API Endpoints
    Additional Information

Project Structure

This project is divided into two main parts:

    Frontend: Built using React/Next.js, handles the user interface and event interactions.
    Backend: Built using NestJS, manages event data and handles CRUD operations in an in-memory database.

Technologies Used

    Frontend: React or Next.js, Axios, React Calendar
    Backend: NestJS, Node.js, TypeScript
    Database: In-memory storage (can be swapped for a persistent database in the future)

Features

    Event CRUD Operations: Create, read, update, and delete events.
    Calendar UI: Displays events on a calendar and allows creating new events by clicking on dates.
    Form Validation: Ensures valid data entry for events.
    Browser Notifications: Sends notifications when event times are reached, with options to snooze or dismiss.
    Search & Filter (Optional): Search and filter events by date or type (text, video, picture).

Setup Instructions
Prerequisites

    Node.js and npm installed
    GitHub or GitLab account (optional for cloning)

Backend Setup

    Clone the backend repository:

git clone <backend-repo-url>
cd calendar-backend

Install dependencies:

npm install

Run the NestJS backend server:

    npm run start

    The backend will be available on a specified port (e.g., http://localhost:3000).

Frontend Setup

    Clone the frontend repository:

git clone <frontend-repo-url>
cd calendar-frontend

Install dependencies:

npm install

Set the backend API URL in the frontend configuration (replace <backend-url>):

const API_URL = '<backend-url>';

Run the React/Next.js frontend:

    npm run dev

    The frontend will be available at http://localhost:3000 or similar, depending on the port.

StackBlitz Setup (Optional)

You can develop both frontend and backend separately on StackBlitz. Follow these steps:

    Create separate projects for the frontend and backend on StackBlitz.
    Set up the backend URL in the frontend configuration to link the two projects.
    Use StackBlitz’s public URLs for testing frontend-backend interactions.

Usage

    Create an Event: Use the form to add event details (title, description, date, time) and submit.
    View Events on Calendar: Added events display on the calendar, organized by date.
    Edit/Delete Events: Use the edit and delete options to update or remove events.
    Browser Notifications: Notifications will pop up at event times, with options to snooze or dismiss.

API Endpoints
GET /events

Fetch all events.
POST /events

Create a new event. Body:

{
  "title": "Event Title",
  "description": "Event Description",
  "date": "YYYY-MM-DD",
  "time": "HH:MM"
}

PUT /events/:id

Update an existing event by id.
DELETE /events/:id

Delete an event by id.
Additional Information

    Form Validation: Required fields include event title, date, and time. Form submissions with incomplete data are prevented.
    Browser Notifications: Notifications are triggered based on event time, with a snooze option for convenience.
    Optional Features: Search and filter options are implemented for additional functionality.
