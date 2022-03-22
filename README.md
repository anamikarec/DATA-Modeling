# DATA-Modeling

#### Ques:~ ***What are valid ways to represent this one-to-many relationship in MongoDB?***

> ***So many different ways are there to mdel 1:N relationship, mainly three we generally use***

> ***Embedding,Linking,Bucketing***
#### Ques:~ What are valid ways on modelling many-to-many relationship with MongoDB?
> ***So many different ways are there to model N:M relationship, mainly two we generally use***

> ***One Way Embedding, Two Way Embedding***
#### Ques:~ What are valid ways to represent a one-to-one relationship with the document model in MongoDB?

> ***So many different ways are there to mdel 1:1 relationship, mainly two we generally use***

> ***Embedding,Linking***


#### Ques:~ create an ERD / CRD diagram for a blog application
> ***the field(columns) that we we choose***
- post_id ```Primary key```
- title
- body
- tags
- comment
- author_name
> ***The post that we will choose will be 1:N, since a post can have so many comments but a comment will be attached to that particular post***

> ***So there will be two schemas, one for posts and second for comments***

> ***Here we will be using linking over embedding***

- Post Collection:~
```js
    post_id: 1,
    title:"",
    body:"",
    tags:"",
    author_name:""
```
- Comment Collection
```js
  post_id: 1,
  comment:"",
  comment_author_name:"",
  comment_date:""
```
#### Ques:~ create and design schema for each collection
> ***the field(columns) that we we choose***
- post_id ```Primary key```
- title
- body
- tags
- comment
- author_name
> ***The post that we will choose will be 1:N, since a post can have so many comments but a comment will be attached to that particular post***

> ***So there will be two schemas, one for posts and second for comments***

> ***Here we will be using linking over embedding***

- Post Collection:~
```js
    post_id: 1,
    title:"",
    body:"",
    tags:"",
    author_name:""
```
- Comment Collection
```js
  post_id: 1,
  comment:"",
  comment_author_name:"",
  comment_date:""
```
#### Ques:~Write a requirement document for designing a system like LinkedIn.
***Schemas to create***
> 
> ***users***
> 
> ***posts***
> 
> ***job_description***
> 
> ***comments***
> 
> ***learnings***

#### Ques:~Estimate daily read and writes, users, data transfer, list down all assumptions you have made

- To do a designing schema for relational data store first we need to follow these steps:-
- List out all the features
- Identify entities related to the feature.


> ***The User should be able to view or edit profile information.***


> ***On the top left the user should have a profile photo***


> ***On the right side of the profile pic, the name and contact information should be displayed.***


> ***A user may send a Connection request to other users. unless the recipient approves the connection request, the sender will just be a follower. once the connection request is accepted, both sender and recipient become followers of each other.***


> ***A user should be able to write a Post.***


> ***A user should be able to Comment on a post or reply to a comment.***


> ***A user should be able to Like a post or a comment.***


#### Ques:~Write down some queries ( no need to write actual queries, but the kind of information that users, and admins would like to see ). for example: - list 10 post by user_id with pagination descending order of date
> ***
