# Spirit of Satoshi Data Cleanup Tool

# Overview
This README file provides an overview of the architecture and components of a SoS Data Cleanup application.

## Architecture
### Backend:
The latest technologies and approaches are used to build the backend as projects must be performance oriented, easily maintainable, and stable.
Tech stack:
NodeJS
PostgreSQL
Stateless REST API
Monolithic architecture

As the application allows users to authenticate using Lightning Login and Nostr, we have orchestration of async requests, webhooks, and subscribers.

The application manages a tremendous amount of data, that is exactly where we use AWS S3 and Lambda orchestration to upload, process and manage datasets without increasing load on the main API.

Due to financial operations, all processes in BE are managed and fully covered/secured by database transactions.

The database fully follows the best practices of relational DB approaches, we use views and stored procedures for heavy operations.

The application uses various algorithms and protection layers to manage huge data streams as several thousands of users are using it simultaneously, we manage that all data input is filtered in scam protection layers and also properly proceeded for honest users.

### Frontend:
Application is built on [Expo](https://expo.dev/ "Expo"), which gives us the excellent capability to have multiple platform apps with a single source code

