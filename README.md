## A GraphQL Server 
Node.js/Express CRUD backend using GraphQL and JSON-Server

### Node modules (dependencies):
- express
- express-graphql
- graphql
- axios (for json server requests)
- json-server (to provide a simple data set)

### Usage
-Install Dependencies
```
$ npm install
```
-Run JSON-Server (Port 3000)
```
$ npm run json:server
```
-Run Server (Port 4000)
```
$ npm run dev:server
```
-Visit Graphiql IDE
```
http://localhost:4000/graphql
```
-Use CRUD requests. examples:
```
// Get data:
{
  customer(id: "3") {
    name,
    email,
    age
  }
}

// Post data:
mutation {
  addCustomer(name: "John Doe", email: "jd@test.com" age: 20) {
    id, name, email, age
  }
}

// Delete data:
mutation {
  deleteCustomer(id: "2") {
    id
  }
}

// Update data:
mutation {
  editCustomer(id: "2", age: 50) {
    id, name, email, age
  }
}
```