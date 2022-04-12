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

Authentication is needed to securely validate the subject identity and it is a crucial precursor to authorization. Authorization policies start after the authentication process completes. The authorization process determines what data you can access.  
```

2. What is the point of a [JSON Web Token](https://jwt.io/introduction)? Why would we want to use it?

```
The session data is stored on the client side and because of that security vulnerabilities emerge. For example, if the user ID is stored in a cookie, it is easy for that user to modify the cookie and change that ID. This will make it possible to get access to someone else’s account. To prevent this we can use JWT
```

3. Why would we hash a user's password when they sign up? What's the point?

```
For security  reasons. We hash passwords to prevent an attacker with read-only access from escalating to higher power levels. Hashing passwords provides defense against your passwords being compromised when a database has been compromised. 
```

4. Go [here](https://jwt.io). Create a JWT with the following as the payload (feel free to change the username/email):

```js
{
  "id": "1",
 "username": "MagJoseph",
  "email": "mag@gamail.co"
}
```

Paste your encoded JWT below:

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjEiLCJ1c2VybmFtZSI6Ik1hZ0pvc2VwaCIsImVtYWlsIjoibWFnQGdhbWFpbC5jbyJ9.X7zzt27lPatbhO4Wv_37M0jE3mi9M9I9vq0g4quK79g
```

**Bonus**: Read https://blog.angular-university.io/angular-jwt

## Submission

Submit a pull request utilizing the [PR Template](https://github.com/SEI-R-2-22/template_pull_request)
