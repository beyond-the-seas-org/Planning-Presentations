# Beyond The Seas

## API Documentation

### Newsfeed

<!--Table for Newsfeed api-->

| API Endpoint                                                                                                     | HTTP Method | Request Body                                                                                                                                                                                                 | Response Code | Response Body                                                                                |
| ---------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------- |
| `GET` Newsfeed                                                                                                     |             |                                                                                                                                                                                                              |               |                                                                                              |
| [beyond-the-seas.org/api/newsfeed/](beyond-the-seas.org/api/newsfeed/)                                                           | GET        | {feed?start=0&count=4 }                                                                                                                                                               | 200           | { "status": "success",<br> "data": { <br> &ensp; "feed": [ { <br> "user_id": 1, <br> "user_name": "Azizur Rahman",<br> "description": "post 1 description", <br>"comments": [] <br> } ]<br> } } | 
| `POST` Add Post |
| [beyond-the-seas.org/api/newsfeed/add-post](beyond-the-seas.org/api/newsfeed/add-post) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "user_name": "Azizur Rahman",<br> &ensp; "description": "post 1 description",<br>} | 201 | {"post": {}} |
| `POST` Add Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/add-comment](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/add-comment) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br> &ensp; "comment": "comment 1",<br>} | 201 | {"comment": {}} |
| `POST` Upvote or Downvote Post |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/upvote](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/upvote) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br> &ensp; "vote": "upvote",<br>} | 201 | {"vote": {}} |
| `POST` Upvote or Downvote Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/upvote](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/upvote) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 , <br> &ensp; "comment_id": 1,  <br> &ensp; "vote": "upvote",<br>} | 201 | {"vote": {}} |
| `POST` Delete Post |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/delete](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/delete) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br>} | 201 | {"post": {}} |
| `POST` Delete Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/delete](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/delete) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 , <br> &ensp; "comment_id": 1,  <br>} | 201 | {"comment": {}} |
| `PUT` Edit Post |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/edit](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/edit) | PUT | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br> &ensp; "description": "post 1 description",<br>} | 200 | {"post": {}} |
| `PUT` Edit Comment |
| [beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/edit](beyond-the-seas.org/api/newsfeed/{user_id}/{post_id}/{comment_id}/edit) | PUT | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 , <br> &ensp; "comment_id": 1,  <br> &ensp; "comment": "comment 1",<br>} | 200 | {"comment": {}} |
| `GET` Get Own Posts |
| [beyond-the-seas.org/api/newsfeed/{user_id}/own-posts](beyond-the-seas.org/api/newsfeed/{user_id}/own-posts) | GET | {<br> &ensp; "user_id": 1,<br>} | 200 | {"posts": {}} |

### Community

<!--Table for Newsfeed api-->

| API Endpoint                                                                                                     | HTTP Method | Request Body                                                                                                                                                                                                 | Response Code | Response Body                                                                                |
| ---------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------- |
| `GET` Community |
| [beyond-the-seas.org/api/community](beyond-the-seas.org/api/community) | GET | {<br> &ensp; "user_id": 1,<br> &ensp; "user_country": "Bangladesh" <br>} | 200 | {"community": {}} |
| `GET` Community Newsfeed |
| [beyond-the-seas.org/api/community/{community_id}/newsfeed](beyond-the-seas.org/api/community/{community_id}/newsfeed) | GET | {<br> &ensp; "user_id": 1,<br> &ensp; "community_id": 2 ,<br> &ensp; "newsfeed": {} <br> } | 200 | {"newsfeed": {}} |
| `GET` Community Members |
| [beyond-the-seas.org/api/community/{community_id}/members](beyond-the-seas.org/api/community/{community_id}/members) | GET | {<br> &ensp; "community_id": 2 <br>} | 200 | {"members": {}} |
| `POST` Join Community |
| [beyond-the-seas.org/api/community/{community_id}/join](beyond-the-seas.org/api/community/{community_id}/join) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "community_id": 2 ,<br>} | 201 | {"join": {}} |
| `POST` Leave Community |
| [beyond-the-seas.org/api/community/{community_id}/leave](beyond-the-seas.org/api/community/{community_id}/leave) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "community_id": 2 ,<br>} | 201 | {"leave": {}} |
| `POST` Add Post |
| [beyond-the-seas.org/api/community/{community_id}/add-post](beyond-the-seas.org/api/community/{community_id}/add-post) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "user_name": "Azizur Rahman",<br> &ensp; "description": "post 1 description",<br>} | 201 | {"post": {}} |
| `POST` Add Comment |
| [beyond-the-seas.org/api/community/{community_id}/{user_id}/{post_id}/add-comment](beyond-the-seas.org/api/community/{community_id}/{user_id}/{post_id}/add-comment) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "post_id": 1 ,<br> &ensp; "comment": "comment 1",<br>} | 201 | {"comment": {}} |
| `POST` Create Community |
| [beyond-the-seas.org/api/community/create](beyond-the-seas.org/api/community/create) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "community_name": "Bangladesh",<br> &ensp; "community_description": "Bangladesh Community",<br> &ensp; "community_country": "Bangladesh",<br>} | 201 | {"community": {}} |
| `POST` Add Member |
| [beyond-the-seas.org/api/community/{community_id}/add-member](beyond-the-seas.org/api/community/{community_id}/add-member) | POST | {<br> &ensp; "user_id": 1,<br> &ensp; "community_id": 2 ,<br> &ensp; "member_id": 3 ,<br>} | 201 | {"member": {}} |
