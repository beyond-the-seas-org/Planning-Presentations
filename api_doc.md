# Beyond The Seas

## API Documentation

### Newsfeed

<!--Table for Newsfeed api-->

| API Endpoint                                                                                                     | HTTP Method | Request Body                                                                                                                                                                                                 | Response Code | Response Body                                                                                |
| ---------------------------------------------------------------------------------------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------------------------- |
| `GET` Newsfeed                                                                                                     |             |                                                                                                                                                                                                              |               |                                                                                              |
| [beyond-the-seas.org/api/newsfeed/](beyond-the-seas.org/api/newsfeed/)                                                           | GET        | {feed?start=0&count=4 }                                                                                                                                                               | 200           | { "status": "success",<br> "data": { <br> &ensp; "feed": [ { <br> &emsp;"user_id": 1, <br>&emsp; "user_name": "Azizur Rahman",<br>&emsp; "description": "post 1 description", <br>&emsp; "comments": [] <br> &ensp;} ]<br> } } | 
 | 