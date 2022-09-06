User Management project enables a user to register themselves into the project. It further gives them the capability to sign in and retrieve the list of all the users who have already registered themselves inside the project.
This repository is responsible for the backend of the project and hosts all the APIs for performing the crud operations on the user database.

The specifications of the project are mentioned below - 

models - user 
user - id, firstname ,lastname, email, password, roles
enum role - ROLE_USER 

repos - userRepo 
security - UserDetailsService, WebConfigurer, 
controller - userController 
             api inside controller - "api/login" , "api/createuser" , "api/userList" 

"/login" 
- GET Method 
- input 

  Request header for Basic Authentication in base64 format
{ 
  "username" : "password" 
}

- output 
{
    "id": 1,
    "firstname" : "abc",
    "lastname" : "user",
    "email" : "xyz@gmail.com",
    "roles" : [
      "ROLE_USER"
    ]
}


"/createuser" 
- POST Method 
- input 
  Request Body
{
    "firstname" : "abc",
    "lastname" : "user",
    "email" : "xyz@gmail.com",
    "password" : "abcddd",
    "roles" : [
      "ROLE_USER"
    ]
}
- output 
{
    "id": 1,
    "firstname" : "abc",
    "lastname" : "user",
    "email" : "xyz@gmail.com",
    "roles" : [
      "ROLE_USER"
    ]
}

"/userList" 
- GET Method 
- input - null 
- output 
{
  {
    "id": 1,
    "firstname" : "abc",
    "lastname" : "user",
    "email" : "xyz@gmail.com",
    "roles" : [
      "ROLE_USER"
    ]
  },
  
  {
    "id": 2,
    "firstname" : "xyz",
    "lastname" : "second_user",
    "email" : "abc@gmail.com",
    "roles" : [
      "ROLE_USER"
    ]
  }
}
