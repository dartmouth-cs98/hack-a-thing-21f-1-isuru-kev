# CRUD API with TypeScript - Backend


## What you built? 

This mini project follows a tutorial on how to build a CRUD API using Typescript, Node and Express. Both of us do not have any experience in Web Development and we thought that this project would be a good introduction to it. The CRUD Api allows users to create, update and delete data about menu items in a restaurant using. The data is stored in a local, in-memory. Express handles the routes that perform the CRUD operations.

Here is the testing we did on the backend via the terminal. We used a series of curl commands to access the in-memory database.

Checking for all items:

```
curl http://localhost:7000/api/menu/items -i
```

<screenshot>
  
Adding a new item:

```
curl -X POST -H 'Content-Type: application/json' -d '{
  "name": "Salad",
  "price": 499,
  "description": "Fresh",
  "image": "https://images.ctfassets.net/23aumh6u8s0i/5pnNAeu0kev0P5Neh9W0jj/5b62440be149d0c1a9cb84a255662205/whatabyte_salad-sm.png"
}' http://localhost:7000/api/menu/items -i
```
  
<screenshot>
  
Updating a new item:

```
curl -X PUT -H 'Content-Type: application/json' -d '{
  "name": "Spicy Pizza",
  "price": 599,
  "description": "Blazing Good",
  "image": "https://images.ctfassets.net/23aumh6u8s0i/2x1D2KeepKoZlsUq0SEsOu/bee61947ed648848e99c71ce22563849/whatabyte_pizza-sm.png"
}' http://localhost:7000/api/menu/items/2 -i
  
curl http://localhost:7000/api/menu/items/2 -i
```
<screenshot>

Deleting an item:

```
curl -X DELETE http://localhost:7000/api/menu/items/2 -i
curl http://localhost:7000/api/menu/items/ -i
```
<screenshot>
  
All curl commands ran succesfful with a 200 status code.



Include some screenshots.
[How?](https://help.github.com/articles/about-readmes/#relative-links-and-image-paths-in-readme-files)

## Who Did What?

Isuru - Worked on initializing the project, setting up the environmental variables. Set up the Typescript interfaces and created a Node.js service and Express Controllers.

Kevin - Set up the Express app and configuration, importing project dependencies and was responsible for testing the Express API Endpoints, Implementing Express Error Handlon and tested the API with a demo client.

## What you learned

Typescript fundamentals: static typing, creating interfaces.
Node.js: handling backend server operations, from the basics such as connecting to a local client. Listening to client responses and handling them.
Express.js: Handling routing in a web app.


## Authors

Isuru Abeysekara, Kevin Cai

## Acknowledgments

CRUD API tutorial - https://auth0.com/blog/node-js-and-typescript-tutorial-build-a-crud-api/

Typescript tutorial - https://www.youtube.com/watch?v=zRo2tvQpus8

https://www.youtube.com/watch?v=BwuLxPH8IDs


