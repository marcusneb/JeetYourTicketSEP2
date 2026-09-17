# JeetYourTicket – Event Ticket Management System

A multi-user, client-server desktop application for listing and selling event tickets, built as the SEP2 semester project at VIA University College.

Admins create and manage events, while multiple users connect at the same time to browse events, filter them, and buy tickets,each purchase generating a unique digital ticket.

## Features

- **Event management (admin):** create, update, and remove events, and monitor ticket sales.
- **Browse & buy (user):** browse listed events, filter by category and city, and purchase tickets.
- **Multiple concurrent clients:** several users can be connected and buying at the same time.
- **Safe ticket sales:** the system never oversells, even when two users try to buy the last ticket at once.
- **Live availability:** ticket counts update in the UI as sales happen.

## Tech Stack

- **Language:** Java 26
- **UI:** JavaFX 
- **Networking:** raw TCP sockets on port 8080, with a custom JSON message protocol (one handler thread per client)
- **Persistence:** PostgreSQL via JDBC
- **Serialization:** Gson

## Getting Started

### Prerequisites

- Java 26 (JDK)
- Java 26 SDK
- PostgreSQL installed and running
- IntelliJ IDEA (the project is set up as an IntelliJ project, not a Maven/Gradle build)

### Database setup

1. Create a PostgreSQL database.
2. Run the schema script: `Sprint 1 Database.sql`.
3. Set the database connection details (URL, username, password) in the server's database class.

### Running the app

Start the server **before** the client, the client checks the connection on startup and will show an error if the server isn't running.

1. Run **`Server.java`** (starts the server on port 8080).
2. Run **`Main.java`** (starts the client UI).
3. Log in as an admin to manage events, or as a user to browse and buy tickets.

## Testing

The system was verified with **72 test cases** covering black-box and white-box testing across the core features.

## Project Context

Developed across six sprints (April–May 2026) as a five-person team using an Agile/Scrum process, from UML design through to a working, tested system. It was the subject of the SWE1-S26 oral exam.

This repository is a personal copy of a team project, shared for portfolio purposes.
