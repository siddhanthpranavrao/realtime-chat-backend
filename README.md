# Simple Chat Application

This is a simple chat application backend built with TypeScript, Node.js, Express, and Socket.io. It provides basic functionality for user authentication, joining a chat room, and sending/receiving messages.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed on your machine.
- [npm](https://www.npmjs.com/) (Node Package Manager) to manage dependencies.

### Installing Dependencies

Run the following command to install project dependencies:

```bash
npm install
```

## Login an existing user:
#### Endpoint: POST /api/auth/login
Request Body:
```json
{
  "username": "example",
  "password": "password"
}
```
Returns a JSON object with the user ID.

## Chat Room
### Retrieve information about the chat room:
#### Endpoint: GET /api/rooms/:roomId
### Join the chat room:
### Endpoint: POST /api/rooms/:roomId/join
Request Body:
```json
{
  "userId": 1
}
```
Returns a JSON object confirming the user has joined.

## Messages
### Retrieve chat history for the chat room:
#### Endpoint: GET /api/rooms/:roomId/messages
### Send a new message to the chat room:
#### Endpoint: POST /api/rooms/:roomId/messages
Request Body:
```json
{
  "userId": 1,
  "text": "Hello, world!"
}
```
Returns a JSON object confirming the message has been sent.
