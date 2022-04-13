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
We want authentication to check the idenity of a user before we provide access to an account in which they will have full access(CRUD) to. 
```

2. What is the point of a [JSON Web Token](https://jwt.io/introduction)? Why would we want to use it?

```
JWT is used to identify a user in a secure way before sharing information to an account. It provides proof of who the user is since JWT is unique for each user. 
```

3. Why would we hash a user's password when they sign up? What's the point?

```
We hash a user's password to protect them from being compromised by a hacker. Hashing takes the password and scrambles it instead of storing it in plaintext. This makes it more difficult for the hacker even if they are able to gain acess to the hashed password.  
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
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjEiLCJ1c2VybmFtZSI6InRpZmZwZXJlaXJhIiwiZW1haWwiOiJ0aWZmcGVyZWlyYUBnbWFpbC5jb20iLCJpYXQiOjE1MTYyMzkwMjJ9.y6IrJU0O6TaXsQM1tACECjekX8_0MsbmIGa-Zi9cpsc
```

**Bonus**: Read https://blog.angular-university.io/angular-jwt

## Submission

Submit a pull request utilizing the [PR Template](https://github.com/SEI-R-2-22/template_pull_request)
