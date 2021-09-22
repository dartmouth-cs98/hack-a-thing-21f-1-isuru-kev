# CRUD API with TypeScript - Backend


## What you built? 

This mini project follows a tutorial on how to build a CRUD API using Typescript, Node and Express. Both of us do not have any experience in Web Development and we thought that this project would be a good introduction to it. The CRUD Api allows users to create, update and delete data about menu items in a restaurant using. The data is stored in a local, in-memory MongoDB database. Express handles the routes that perform the CRUD operations.

Include some screenshots.
[How?](https://help.github.com/articles/about-readmes/#relative-links-and-image-paths-in-readme-files)
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


## Authors

Isuru Abeysekara, Kevin Cai

## Acknowledgments

CRUD API tutorial - https://auth0.com/blog/node-js-and-typescript-tutorial-build-a-crud-api/

Typescript tutorial - https://www.youtube.com/watch?v=zRo2tvQpus8

https://www.youtube.com/watch?v=BwuLxPH8IDs


