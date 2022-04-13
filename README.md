# Authentication Study

Please take the time to read this [article](https://medium.com/ag-grid/a-plain-english-introduction-to-json-web-tokens-jwt-what-it-is-and-what-it-isnt-8076ca679843) before proceeding.

## Instructions

- Fork and Clone

Write your answers in the space provided in this readme.

## A Note on Passwords

We **never** store passwords in our database. Instead, we use a hashing function to create a password hash or digest. We store the password digest in our database.

![](password_digest.jpeg)

## JSON Web Token (JWT) Authentication

Here is a flow for using JWT for Authentication

![](jwt.jpeg)

1. The user signs up:

- The client creates a POST request to the `/signup` endpoint on the server with username, email, and password in the request body

2. The server creates a JSON Web Token (JWT) based on a header, payload, and secret
3. The server responds with the JWT
4. The client saves the JWT in localStorage to persist subsequent server requests

##

Answer the following questions:

1. Why do we need authentication in our Web Apps?

```
Authentication allows us to provide personalized content to multiple users, for example shopping carts or posts/comments. We need authentication to prevent one user from accessing the data of another user.  
```

2. What is the point of a [JSON Web Token](https://jwt.io/introduction)? Why would we want to use it?

```
JSON Web Tokens are used to streamline the authentication process by obviating the need to check the server for the users credentials with every request. Instead, the JWT is stored locally (client-side) and is sent with each request to verify the user's identity when accessing their data. 
```

3. Why would we hash a user's password when they sign up? What's the point?

```
Passwords should always be hashed so that they cannot be read as plain text by anyone who might have access (with or without permission) to data stored in a database. 
```

4. Go [here](https://jwt.io). Create a JWT with the following as the payload (feel free to change the username/email):

```js
{
  "id": "1",
  "username": "bruno",
  "email": "bruno@ga.co"
}
```

Paste your encoded JWT below:

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjEiLCJ1c2VybmFtZSI6ImJydW5vIiwiZW1haWwiOiJicnVub0BnYS5jbyJ9.SNHM7vL6ehTkvM4Rg-IH-SanpKkCN3KtQ68qESpkcZU
```

**Bonus**: Read https://blog.angular-university.io/angular-jwt

## Submission

Submit a pull request utilizing the [PR Template](https://github.com/SEI-R-2-22/template_pull_request)
