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

We were able to retrieve all the items stored in the database using the command:
curl http://localhost:7000/api/menu/items -i
This is shown in /images/GetAllItems.png

We were able to retrieve a single item using the command:
curl http://localhost:7000/api/menu/items/2 -i
This is shown in /images/GetOneItem.png

From the terminal we added an item using the command:
curl -X POST -H 'Content-Type: application/json' -d '{
  "name": "Salad",
  "price": 499,
  "description": "Fresh",
  "image": "https://images.ctfassets.net/23aumh6u8s0i/5pnNAeu0kev0P5Neh9W0jj/5b62440be149d0c1a9cb84a255662205/whatabyte_salad-sm.png"
}' http://localhost:7000/api/menu/items -i
This is shown in /images/AddItem.png

We were able to verify that the new item was added using:
curl http://localhost:7000/api/menu/items/ -i
Shown in /images/VerifyAddedItem.png

## Who Did What?

Isuru - Worked on initializing the project, setting up the environmental variables. Set up the Typescript interfaces and created a Node.js service and Express Controllers.

Kevin - Set up the Express app and configuration, importing project dependencies and was responsible for testing the Express API Endpoints, Implementing Express Error Handlon and tested the API with a demo client.

## What you learned

Typescript fundamentals: static typing, creating interfaces.
Node.js: handling backend server operations, from the basics such as connecting to a local client. Listening to client responses and handling them.
Express.js: Handling routing in a web app.


## What can we do in the future?
  
We were thinking of setting up a frontend for this project but we did not have the time to do it. To begin with, we could use EJS to establish a consistent theme across all web pages in the UI once a create, update, or delete command is used. It would also be beneficial to display the list of items in memory to show that the commands worked. We presume that React could be used here too and would lead to a much better frontend too.

In terms of the backend, we could use a MongoDB database, or a PostGRES sql database to store this information. In-memory storage is often limited and is refreshed every single time that we started up the server so there was a lot of data that we used to test the backend with was lost. A MongoDB Atlas database is very easy to set up and is free of charge for one time use. 
https://docs.atlas.mongodb.com/getting-started/
  
Something that went wrong during this mini project was that we were not used to typescript syntax and its static typing features. We often ran into problems where we forgot to cast Exceptions as types - we were simply unaware that most things in typescript had a type. Hopefully, with more coding experience, we will get used to it and code better!
  


## Authors

Isuru Abeysekara, Kevin Cai

## Acknowledgments

CRUD API tutorial -    https://auth0.com/blog/node-js-and-typescript-tutorial-build-a-crud-api/

Typescript tutorials - https://www.youtube.com/watch?v=zRo2tvQpus8 , https://www.youtube.com/watch?v=BwuLxPH8IDs


