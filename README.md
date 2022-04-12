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
We need authentication to ensure that an app's users can access specific information/app functionality, and to ensure that non-authenticated users have limited or restricted access.
```

2. What is the point of a [JSON Web Token](https://jwt.io/introduction)? Why would we want to use it?

```
A JSON Web Token, or JWT, provides a secure container for data exchanged through a network. A JWT is used to protect information that is being transferred.
```

3. Why would we hash a user's password when they sign up? What's the point?

```
We want to prevent anyone with access to the database from stealing the password/tampering with it, which would be possible if the password was stored directly in the database without a hash appended to it. We want to protect a user's password.
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
<--- ANSWER GOES HERE --->
```

**Bonus**: Read https://blog.angular-university.io/angular-jwt

## Submission

Submit a pull request utilizing the [PR Template](https://github.com/SEI-R-2-22/template_pull_request)
