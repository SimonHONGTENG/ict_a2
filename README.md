# A2 Chat Application

## Layout of GIT Repository

SRC

1. App (frontend)
- Chat (Channel)
- Groups
- Group-Details (Channel list)
- Users (all the users in the system)
- Profile (profile of user)
- User-detail (edit mode of user)

2. Server (backend)
- API (CRUD)
  * channels.js (channels api)
  * groups.js (groups api)
  * users.js (users api)
- index.js
- socket.js
    

## GIT Process Approach

The layout of GIT Repo: it's a standard Angular project, and with backend Node/Express in server folder under Angular APP folder.
The angular part has several components and routing and node side has all the api file with routing as well. 

The process of version control is: Create a remote GitHub project, and clone one on local PC, branch from master for front end, and develop the front end with in-mermory data store, tested all ok, merge back to master, and then push back to remote in GitHub. Do the sam ething for the backend to build all the REST APIs, test each REST API in Postman to make sure they are all working as expected before commit and merge into master.  

## Data Structures

User entity has username as primary key, has stored the array of channels id for which the user belonbgs to. it also stores email address and another flaag to indicate if they are group admin themself.

Group entity has an id as it primary key, and groupname.

Channel entity has an id as it primary key, and groupname.

## REST API
---
[Users](users.md) <br/>
[Groups](groups.md) <br/>
[Channels](channels.md) 

## Angular Architecture

Angular front end has a few components like login, groups, channels and users, all the components located within the app shell, it also include groups, channnels, users and message services to do the data CRUD mapping, the message service is purely used for information or debguging purpose. 
The models in Angular has user, group and channel which are reflected with the backend entities.

## State Change

MongoDB has been used for storing backend data.


