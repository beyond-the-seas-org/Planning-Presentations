# Beyond The Seas

## API Documentation

### Newsfeed

<!--Table for Newsfeed api-->

| API Endpoint                                                                                                     | HTTP Method | Request Body                                                                                                                                                                                                 | Response Code | Response Body                                                                                |
| ---------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------- |
| `GET` Newsfeed                                                                                                     |             |                                                                                                                                                                                                              |               |                                                                                              |
| [beyond-the-seas.org/api/newsfeed/feed?start=0&count=4](beyond-the-seas.org/api/newsfeed/feed?start=0&count=4)                                                           | GET        | {}                                                                                                                                                               | 200           | { "status": "success",<br> "data": { <br> &ensp; "feed": [ { <br> "user_id": 1, <br> "user_name": "Azizur Rahman",<br> "description": "post 1 description", <br>"comments": [] <br> } ]<br> } } | 
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
| `GET` Provide Analytics Data to Analytics Service |
| [beyond-the-seas.org/api/newsfeed/analytics](beyond-the-seas.org/api/newsfeed/analytics) | GET | {} | 200 | {"analytics": {}} |

### Community

<!--Table for Community api-->

| API Endpoint                                                                                                     | HTTP Method | Request Body                                                                                                                                                                                                 | Response Code | Response Body                                                                                |
| ---------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------- |
| `GET` Community |
| [beyond-the-seas.org/api/community](beyond-the-seas.org/api/community) | GET | {<br> &ensp; "user_id": 1,<br> &ensp; "user_country": "Bangladesh" <br>} | 200 | {"community": {}} |
| `GET` Community Newsfeed |
| [beyond-the-seas.org/api/community/{community_id}/newsfeed/feed?start=0&count=4](beyond-the-seas.org/api/community/{community_id}/newsfeed/feed?start=0&count=4) | GET | {<br> &ensp; "user_id": 1,<br> &ensp; "community_id": 2 <br> } | 200 | {"newsfeed": {}} |
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
| `GET` Provide Analytics Data For Analytics Service |
| [beyond-the-seas.org/api/community/analytics](beyond-the-seas.org/api/community/analytics) | GET | {} | 200 | {"analytics": {}} |

### Analytics

<!--Table for Analytics api-->

| API Endpoint                                                                                                     | HTTP Method | Request Body                                                                                                                                                                                                 | Response Code | Response Body                                                                                |
| ---------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------- |
| `GET` Analytics based on Professors' short list |
| [beyond-the-seas.org/api/analytics/professors-short-list](beyond-the-seas.org/api/analytics/professors-short-list) | GET | {<br>"professors":{}} | 200 | {"analytics": {}} |
| `GET` Analytics Data From Newsfeed |
| [beyond-the-seas.org/api/analytics/newsfeed](beyond-the-seas.org/api/analytics/newsfeed) | GET | {} | 200 | {"newsfeed_analytics": {}} |
| `GET` Analytics Data From Community |
| [beyond-the-seas.org/api/analytics/community](beyond-the-seas.org/api/analytics/community) | GET | {} | 200 | {"community_analytics": {}} |
| `GET` Analytics Data From User Profile |
| [beyond-the-seas.org/api/analytics/user-profile](beyond-the-seas.org/api/analytics/user-profile) | GET | {<br>"user_id":1<br>} | 200 | {"profile_analytics": {}} |
| `GET` Professor Data based on Research Area |
| [beyond-the-seas.org/api/analytics/professor](beyond-the-seas.org/api/analytics/professor) | GET | {<br>"research_area":"Computer Science"<br>} | 200 | {"professors": {}} |
|`POST` Give Analytics Criteria |
| [beyond-the-seas.org/api/analytics/give-criteria](beyond-the-seas.org/api/analytics/give-criteria) | POST | {<br>"user_id":1, <br>"weather":"Moderate", <br> "living_cost":{[1000,2000]}, <br> "community":"Large", <br> "crime_rate": [0.5, 2], <br>"field_of_interest":{["Network", "Cyber Security"]},<br> "jobs": true, <br> "public transportation": true}, <br> "health_care_facilities": true | 201 | {"criteria": {}} |
| `GET` Preference Analysis Data |
| [beyond-the-seas.org/api/analytics/preference-analysis](beyond-the-seas.org/api/analytics/preference-analysis) | GET | {<br>"user_id":1, <br>"newsfeed_analytics":{}, <br> "community_analytics":{}, <br> "profile_analytics":{}, <br> "professors":{}<br>} | 200 | {"preference-analysis": {}} |





