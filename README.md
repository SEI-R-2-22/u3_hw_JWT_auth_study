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
Requiring authentication is important if the web app requires personal or sensitive information. It is also helpful in apps that assign data to a user. Authentication verifies the identity of the user so that they can proceed with the app.
```

2. What is the point of a [JSON Web Token](https://jwt.io/introduction)? Why would we want to use it?

```
The definition given in the article is that a JWT is a standardized, optionally validated and/or encrypted container format that is used to securely transfer information between two parties. It being referred to as a container format describes the structure of the information being sent across the network. It has a serialized and deserialized components, with the former being used to transfer data through the network and the former to read and write data to the token.
```

3. Why would we hash a user's password when they sign up? What's the point?

```
The cryptographic hash function produces a signature that is used to verify the message when signing up. It is an additional layer of security because both parties (the user and the site) can generate that signature to verify.
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
