We have a demo api to signup, login and retrieve logged-in user's profile

```
Mandatory headers required in each request 
  X-Parse-Application-Id: 1aKNPKlZZkL3gKe1avjN4bJzq1pkgAw7vj2aLRO3
  X-Parse-REST-API-Key:  ibV2rrC1p90TfLxwUumNkKAzI7Rgk49bCj4ODnLV
```


**Signup**
```
POST: https://parseapi.back4app.com/users
payload/body: {"username: "something", "password": "anything"}

sample payload:
{
    "objectId": "PJoZRR7SCa",
    "createdAt": "2020-11-04T15:23:08.945Z",
    "sessionToken": "r:6e68b0ef7733ad34d0871927c8df23f9"
}
```

**Login**
```
POST: https://parseapi.back4app.com/login
payload/body: {"username: "something", "password": "anything"}

sample payload:
{
    "objectId": "PJoZRR7SCa",
    "createdAt": "2020-11-04T15:23:08.945Z",
    "createdAt": "2020-11-04T15:12:08.535Z",
    "updatedAt": "2020-11-04T15:12:08.535Z",
    "sessionToken": "r:6e68b0ef7733ad34d0871927c8df23f9",
    "ACL": "{...}"
}
```

**Get Logged in user's profile**
```
GET: https://parseapi.back4app.com/users/me

additional header:
X-Parse-session-token: "r:6e68b0ef7733ad34d0871927c8df23f9" // do not use this value. use the sessionToken you received during login/signup

sample payload:
{
    "objectId": "PleiF47pGA",
    "username": "faysal",
    "createdAt": "2020-11-04T15:12:08.535Z",
    "updatedAt": "2020-11-04T15:12:08.535Z",
    "ACL": {...},
    "__type": "Object",
    "className": "_User",
    "sessionToken": "..."
}
```


# Task

You are required to build a next.js(10) app which will have the functionalities given above in the form of api request. Logged in users should be able to view his profile.

Your app will contain the follwing pages
1. `/signup` and login (can be 2 page or single page)
2. `/` page. This just show you're logged in. Users will be redirected in this page after login/signup
3. `/profile` need to see the user profile.

This is a fairly simple app. We don't want to see how good the UI looks(because we know you can make good UI). Your project will be evaluated 
based on the following criteria

1. Coding Standards.
2. Proper use of available libraries and state managements
3. Properly handling errors and showing errors
4. Validations



