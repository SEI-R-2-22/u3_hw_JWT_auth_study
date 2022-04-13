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
We use authentication in Apps in order to provide a talored experience to said users. An example can be if multiple request are made, those request will be associated with that user.
```

2. What is the point of a [JSON Web Token](https://jwt.io/introduction)? Why would we want to use it?

```
JWT allow the transmission of information between the client-side and server-side to be secured using a signature. This signature allows the server to verify the authenticity of the session data. 
```

3. Why would we hash a user's password when they sign up? What's the point?

```
You don't want to store the password in plain text. For example, the package can be intercepted when going fron client-to-server or server-to-client via a man in the middle attack. An individual snooping on your network would be able to read in plain english your username/password. By hashing the password, it encrypts the information so even though it may land on the wrong hands, they may not be able to use the decode the header/package. 
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
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjEiLCJ1c2VybmFtZSI6ImJydW5vIiwiZW1haWwiOiJicnVub0BnYS5tYWlsLmNvIn0.0Kg5oWaxM3CtjQakyPKO312aT1xtnAjlUND7bFxTQZM
```

**Bonus**: Read https://blog.angular-university.io/angular-jwt

## Submission

Submit a pull request utilizing the [PR Template](https://github.com/SEI-R-2-22/template_pull_request)
