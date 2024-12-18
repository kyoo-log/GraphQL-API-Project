# GraphQL API with Node.js, Apollo Server, and MongoDB

## Description
This project demonstrates the implementation of a GraphQL API built with Node.js, Apollo Server, and MongoDB. It handles user queries efficiently and supports real-time updates via GraphQL subscriptions.

## Features
- Query users from the MongoDB database
- Add new users with mutations
- Real-time user updates using subscriptions

## Technologies
- **Node.js**: JavaScript runtime environment
- **Apollo Server**: GraphQL server implementation
- **MongoDB**: NoSQL database for storing user data
- **Subscriptions-transport-ws**: WebSocket for real-time communication
- **Mongoose**: ODM for MongoDB

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/graphql-api.git
   cd graphql-api
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure MongoDB connection:
   - Create a `.env` file in the root directory and add your MongoDB URI:
     ```
     MONGO_URI=mongodb://localhost:27017/graphql-db
     PORT=4000
     ```

4. Run the server:
   ```bash
   npm start
   ```

5. Open the Apollo Server playground in your browser at `http://localhost:4000` to interact with the API.

## GraphQL Queries

### Query to fetch all users:
```graphql
query {
  getUsers {
    id
    name
    email
    age
  }
}
```

### Mutation to add a new user:
```graphql
mutation {
  addUser(name: "John Doe", email: "john.doe@example.com", age: 28) {
    id
    name
    email
    age
  }
}
```

### Subscription to get real-time updates when a new user is added:
```graphql
subscription {
  userAdded {
    id
    name
    email
    age
  }
}
```

## Contributing
Feel free to fork the repository, create issues, and submit pull requests for any improvements or features you would like to add.

## License
MIT License