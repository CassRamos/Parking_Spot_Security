<h1 align="center"> Parking Spot Security  </h1>

<p align="center">
Utilizing Spring Security in a previous application <br/>
</p>

<p align="center">
  <a href="#-tecnologies">Tecnologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-project">Project</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-license">License</a>
</p>


<br>

## 🚀 Tecnologies

This project was developed with the following technologies:

- Java
- Spring framework 🍃 - Spring Security, Spring Data JPA, Spring Validation & Spring Web
- Postgres 🐘
- Git & Github 
- Postman


## 💻 Project

The Parking Spot is an application responsible for implementing a CRUD along with validations to simulate a registration in a parking space. In this extension. we use Spring Security to authorize users (by role) to use certain endpoints 


## :memo: License

This project is under license from MIT

<br>


## Database 
  - User table contains a password encoded and a UUID (i use the UUID generator):
<p align="center">
  <img alt="Table User" src="./img/tb_user.png" width="80%">
</p>
- Here is the password in code and the password encoded in terminal:
<p align="center">
  <img alt="Pass" src="./img/default_pass.png" width="80%">
  <img alt="Pass encoded" src="./img/console_pass.png" width="80%">
</p>

- Roles table contains only 2 roles to determine access to certain endpoints in application (i used the UUID generator again for the role_id field) :
<p align="center">
  <img alt="Roles" src="./img/tb_role.png" width="40%">
</p>

- Table users_roles is responsible for matching the user to their role, allowing exclusive access to certain methods:
<p align="center">
  <img alt="Roles & Users" src="./img/tb_users_roles.png" width="60%">
</p>

- Here is the config of endpoints:
<p align="center">
  <img alt="Access to endpoints" src="./img/endpoint_acess.png" width="40%">
</p>

<br>

## Endpoints 📡

<br>

### GET 
  - All info about the registered spots:
  - This endpoint is allowed to all roles in db
<p align="center">
  <img alt="Get all" src="./img/get_all.png" width="60%">
</p>

  - Using the wrong password the access is denied
<p align="center">
  <img alt="Get all failed" src="./img/failed_get_all.png" width="60%">
</p>

<br>

### POST 
  - Register a spot:
  - This method is only allowed for the role USER 
<p align="center">
  <img alt="Post spot" src="./img/user_post.png" width="60%">
</p>

  - If the ADMIN tries to access the method... 
<p align="center">
  <img alt="Post failed" src="./img/admin_post.png" width="60%">
</p>

<br>

### Update ⚙ (PUT):
  - Updating by id:
  - Only allowed to ADMIN role
<p align="center">
  <img alt="Updating" src="./img/admin_update.png" width="60%">
</p>

  - If the USER tries to access the method... 
<p align="center">
  <img alt="Update failed" src="./img/user_post.png" width="60%">
</p>

<br>

### Delete ❌:
  - Deleting by id:
  - Only allowed to ADMIN role
<p align="center">
  <img alt="Delete by id" src="./img/admin_delete.png" width="60%">
</p>

 - If the USER tries to access the method... 
<p align="center">
  <img alt="Delete failed" src="./img/user_delete.png" width="60%">
</p>

<br> 

### Thanks for your attention, see you next time 💜






