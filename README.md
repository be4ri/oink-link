# **Oink Link**

## ***Description***

Oink Link is a fun and easy way to share your thoughts and post messages for everyone to see. Explore what others are up to, and  search posts based on a specific category that interest you, like music, movies or sports. Join the discussion, see what's trending and comment on posts you find interesting.  

## ***Entities***

***Post***
 - id: unique identifier for a post
 - userID: foreign key of the user who created the post
 - title (string): the title of the post - [between 1-50 characters]
 - postText (string): The text of the post - [between 1-500 characters]
 - datePosted (date and time): The date the post was posted
 - likes (int): The number of likes the post has (default is 0)
 - category (foreign key): a category from the predefined categories

***Comment***
 - id: unique identifier for a comment
 - userID: foreign key of the user who created the post
 - postID: foreign key of the post 
 - commentText (string): The user's comment - [between 1-100 characters]

***User***
 - id: unique identifier for the user
 - username: the username of the user - [unique, between 1-15
   characters]
 - email (string): the email of the user [unique]
 - password (string): The password of the user's account [should
   contain: one number, one big letter (?), should be between 8-30   
   characters long]
 - description (string): The description of the user's profile [between
   0-100 characters]

***Category***
 - id: unique identifier for the category
 - categoryName: the name of the category (ex. Sports, Daily, Trending etc.)

 *Categories are predefined and each post can be a part of one category*

## ***CRUD operations***

 ***Post***
 - CREATE: A user can create a post by introducing the following fields: title, postText, image (optional).
   - **offline**: *The post awaits internet in order to be sent, the user will get a message with "The post will get posted once the internet connection is established"*
 - READ: The user should be able to see all post made by other users
   - **offline**: *The user will not see any posts and the user will get an error with "No internet connection, unable to see the posts"*
 - UPDATE: The user should be able to update the title and the text of a post created by him.
    - **offline**: *The post awaits interned in order to get updated, the user will get a message with "The post will get updated once the internet connection is established"*
 - DELETE: The user should be able to delete only a post created by him.
     - **offline**: *The post awaits internet in order to be deleted and the user will get a message with "The post will get deleted once the
   internet connection is established" *

All operations: CREATE, UPDATE, DELETE will be persisted on the db and on the server.

***Comment***
 - CREATE: The user can add a comment under any post
    - **offline**: *The comment will not get posted and the user will get an error "No internet connection"*
 - READ: The user will be able to see all the comments from a post under the specific post
     - **offline**: *The user will not see any posts, therefore no comments and will get the error from the READ posts"*
 
 ***User***
 - CREATE: The user should be able to register by introducing a username (should be unique), an email and a password. The description field will initially be empty.
     - **offline**: *The user will not be able to create an account and he will get an error "No internet connection"*
 - UPDATE: The user should be able to change the description directly from the profile. The user can change the username, password or email from the settings (from the profile).
     - **offline**: *The user will not be able to update the account and he will get an error "No internet connection"*
 - DELETE: The account cannot be deleted :(
 
 The operations: CREATE, UPDATE will be persisted on the db and on the server.

***Category***
Categories are predefined, and they cannot be created, updated or deleted by the user.

## ***Figma***

 - Login
 <img width="726" height="1221" alt="login-figma" src="https://github.com/user-attachments/assets/cfd1f650-0a4c-447c-8acf-28e0ba9e29c0" />
 
 - List of posts
 <img width="710" height="1188" alt="list-of-posts-figma" src="https://github.com/user-attachments/assets/ff095aa6-d6ac-415e-a90d-35a8375f09be" />

 - One Post from the List
 <img width="686" height="1191" alt="one-post-figma" src="https://github.com/user-attachments/assets/977e7951-fa2e-4e20-94ae-d366c50f5a56" />

 - Create a post
 <img width="724" height="1198" alt="create-post-figma" src="https://github.com/user-attachments/assets/5091ce23-08fc-42b1-8b97-040722d972e5" />
 
 - Edit and Delete
 <img width="687" height="1209" alt="update-and-delete-post-figma" src="https://github.com/user-attachments/assets/7e86a196-b4e2-41f6-a508-b84409891fab" />




 
 

 
