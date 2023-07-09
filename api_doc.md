# Beyond The Seas

## API Documentation

### Newsfeed

<!--Table for Newsfeed api-->

| API Endpoint                                                                                                     | HTTP Method | Request Body                                                                                                                                                                                                 | Response Code | Response Body                                                                                |
| ---------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------- |
| `GET` Newsfeed                                                                                                     |             |                                                                                                                                                                                                              |               |                                                                                              |
| [beyond-the-seas.org/api/newsfeed/](beyond-the-seas.org/api/newsfeed/)                                                           | GET        | {feed?start=0&count=4 }                                                                                                                                                               | 200           | { "status": "success",<br> "data": { <br> &ensp; "feed": [ { <br> &emsp;"user_id": 1, <br>&emsp; "user_name": "Azizur Rahman",<br>&emsp; "description": "post 1 description", <br>&emsp; "comments": [] <br> &ensp;} ]<br> } } | 
| `POST` Add Post |
| [beyond-the-seas.org/api/newsfeed/](beyond-the-seas.org/api/newsfeed) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "user_name": "Azizur Rahman",<br> &ensp; "description": "post 1 description",<br>} | 200 | {"post": {}} |
| `POST` Add Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/add-comment](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/add-comment) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br> &ensp; "comment": "comment 1",<br>} | 200 | {"comment": {}} |
| `POST` Upvote or Downvote Post |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/upvote](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/upvote) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br> &ensp; "vote": "upvote",<br>} | 200 | {"vote": {}} |
| `POST` Upvote or Downvote Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/upvote](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/upvote) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 , <br> &ensp; "comment_id": 1,  <br> &ensp; "vote": "upvote",<br>} | 200 | {"vote": {}} |
| `POST` Delete Post |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/delete](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/delete) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br>} | 200 | {"post": {}} |
| `POST` Delete Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/delete](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/delete) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 , <br> &ensp; "comment_id": 1,  <br>} | 200 | {"comment": {}} |
| `PUT` Edit Post |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/edit](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/edit) | PUT | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br> &ensp; "description": "post 1 description",<br>} | 200 | {"post": {}} |
| `PUT` Edit Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/edit](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/edit) | PUT | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 , <br> &ensp; "comment_id": 1,  <br> &ensp; "comment": "comment 1",<br>} | 200 | {"comment": {}} |
| `GET` Get Own Posts |
| [beyond-the-seas.org/api/newsfeed/{user_id}/own-posts](beyond-the-seas.org/api/newsfeed/{user_id}/own-posts) | GET | {<br> &ensp; "user_id": 1,<br>} | 200 | {"posts": {}} |

