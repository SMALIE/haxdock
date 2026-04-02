# Backend

## Overview

This documentation provides information about the backend for the HaxDock project. The backend is implemented using NestJS, MongoDB as the database, Prisma for data access, and GraphQL for API queries and mutations. The purpose of the backend is to handle player-related operations, including authentication, player updates, and retrieving player data.

![Server Diagram](../docs/architecture-server.jpg)

## Getting Started

Follow these steps to set up and run the project:

1. Install dependencies:
    ```bash
    npm install
    ```

2. Run the development server:
    ```bash
    npm run start:dev
    ```

## Functionality

The backend facilitates various player-related operations through GraphQL queries. The primary functionalities include:

- User authentication (`authorization` query)
- Player creation and update (`upsertPlayer` mutation)
- Retrieving player room states (`roomsState` query)
- Updating player information (`updatePlayer` mutation)
- Updating room states (`updateRoomState` mutation)
- Retrieving a list of players (`getPlayers` query)

## Environment Variables

Ensure you have the following environment variables set in your `.env` file:

```bash
DATABASE_URL="mongodb+srv://your_username:your_password@cluster0.kq8ginl.mongodb.net/haxstars?retryWrites=true&w=majority"
JWT_PASSWORD=your_jwt_password
JWT_SECRET=your_jwt_secret
```

Replace placeholders like `your_username`, `your_password`, `your_jwt_password`, and `your_jwt_secret` with your actual values.

## Authentication

Authentication is required for certain mutations and queries. The `AuthGuard` is used to ensure that only authenticated users can access protected queries.

## Scripts

- `build`: Build the NestJS project.
- `start`: Start the NestJS server.
- `start:dev`: Start the server in development mode with watch.
- `start:debug`: Start the server in debug mode with watch.
- `start:prod`: Start the server in production mode.
- `test`: Run Jest tests.
- `test:watch`: Run Jest tests in watch mode.
- `test:e2e`: Run end-to-end tests using Jest.
