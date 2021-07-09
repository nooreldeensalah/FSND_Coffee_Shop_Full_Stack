# Notes to the reviewer:

- The project dependencies are fairly messed up, here is what I did to get it working with the help of [this topic](https://knowledge.udacity.com/questions/464138) on Udacity.
    - I'm using `Python 3.9` and updated `requirements.txt` until I got the project in a functional state.
    - After installing frontend dependencies, I ran the following two commands:
        - `npm uninstall node-sass`
        - `npm install node-sass@4.14.1`
    
- I have made some changes to the postman testing collection:
    - Changed `Barista` `POST /drinks` endpoint authorization to inherit from parent.
    - Updated the request body for `manager` `POST /drinks` endpoint because it was malformed, I made a request from the frontend, and copied it from the network tab in browser dev tools.
- I have created two users on my auth0 domain, here are their details:

### Barista
```
id/email : barista@example.com
password : k?:2@(zcGXY3(aw}
```

### Manager

```
id/email: manager@example.com
password: k?:2@(zcGXY3(aw}
```
- I also made sure to update the tokens and exporting them to the collection before submitting the project.

# Coffee Shop Full Stack

## Full Stack Nano - IAM Final Project

Udacity has decided to open a new digitally enabled cafe for students to order drinks, socialize, and study hard. But they need help setting up their menu experience.

You have been called on to demonstrate your newly learned skills to create a full stack drink menu application. The application must:

1. Display graphics representing the ratios of ingredients in each drink.
2. Allow public users to view drink names and graphics.
3. Allow the shop baristas to see the recipe information.
4. Allow the shop managers to create new drinks and edit existing drinks.

## Tasks

There are `@TODO` comments throughout the project. We recommend tackling the sections in order. Start by reading the READMEs in:

1. [`./backend/`](./backend/README.md)
2. [`./frontend/`](./frontend/README.md)

## About the Stack

We started the full stack application for you. It is designed with some key functional areas:

### Backend

The `./backend` directory contains a partially completed Flask server with a pre-written SQLAlchemy module to simplify your data needs. You will need to complete the required endpoints, configure, and integrate Auth0 for authentication.

[View the README.md within ./backend for more details.](./backend/README.md)

### Frontend

The `./frontend` directory contains a complete Ionic frontend to consume the data from the Flask server. You will only need to update the environment variables found within (./frontend/src/environment/environment.ts) to reflect the Auth0 configuration details set up for the backend app.

[View the README.md within ./frontend for more details.](./frontend/README.md)
