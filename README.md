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
it helps with interactions between the person and web app, restricts users from sensitive content
we need authentication so th
<--- ANSWER GOES HERE --->
```

2. What is the point of a [JSON Web Token](https://jwt.io/introduction)? Why would we want to use it?

``
a JWT is used to encrypt data, make it not as easy to be tampered with, also it is compact & can be sent with post
<--- ANSWER GOES HERE --->

````

3. Why would we hash a user's password when they sign up? What's the point?

```because passwords should neveer be stores in DB, & there is no need for plain text passwords to be saved
<--- ANSWER GOES HERE --->
````

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
eyJhbGciOiJIUzI1NiJ9.eyJpZCI6IjEiLCJ1c2VybmFtZSI6ImJydW5vIiwiZW1haWwiOiJicnVub0BnYS5jbyJ9.YfnkU1z5pJ7aSDOv6Mg_h1aA-tRrEq6T-0QhRldzlp4
<--- ANSWER GOES HERE --->
```

**Bonus**: Read https://blog.angular-university.io/angular-jwt

## Submission

Submit a pull request utilizing the [PR Template](https://github.com/SEI-R-2-22/template_pull_request)
