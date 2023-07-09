# API Documentation

<!-- create tables for api documentation -->

## Authentication

| Endpoint | Method | Request Body | Response Code | Response Body |
| --- | --- | --- | --- | --- |
| ```POST``` Login | | | | |
| http://beyond-the-seas.org/login/ | POST | ```{ "username": "string", "password": "string" }``` | 200 | ```{ "token": "string" }``` |
| ```GET``` Logout | | | | |
| http://beyond-the-seas.org/logout/ | GET | | 200 | |


## User Profile
<!-- endpoint format: http://beyond-the-seas.org/api/user/ -->
<!-- Beutify the response body so that it looks like JSON format -->

| Endpoint | Method | Request Body | Response Code | Response Body |
| --- | --- | --- | --- | --- |
| ```POST``` Create User | | | | |
| http://beyond-the-seas.org/api/user/create | POST | ```{ "username": "string", "password": "string", "email": "string", "first_name": "string", "last_name": "string", "gender": "string", "age": "string"}``` | 201 | |
| ```POST``` Update User Profile | | | | |
| http://beyond-the-seas.org/api/user/{user_id}/update-profile | POST | ``` { "user_id": "string", "bsc-varsity": "string", "bsc-year": "string", "msc-varsity": "string", "msc-year": "string", "bsc-cgpa": "string", "msc-cgpa": "string", "gre-score": [], "language-score": [], "github-link": "string", "linkedin-link": "string", "personal-site": "string", "publication-link": [] } ``` | 200 | ``` { "profile": {} } ``` |
| ```GET``` User Profile | | | | |
| http://beyond-the-seas.org/api/user/{user_id}/profile | GET | ```{ "user_id": "string" }``` | 200 | ```{ "profile": {} }``` |

## Professor
<!-- endpoint format: http://beyond-the-seas.org/api/professor/ -->

| Endpoint | Method | Request Body | Response Code | Response Body |
| --- | --- | --- | --- | --- |
| ```GET``` Search Professor | | | | |
http://beyond-the-seas.org/api/professor/search?start=0&count=10 | GET | ```{ "keyword": "string" }``` | 200 | ```{ "professors": [{ "name": "string", "designation": "string", "department": "string", "research_area": [], "email": "string", "address": "string", "website": "string", "scholar_info": "string" }, {}] }``` |
| ```GET``` Professor Details | | | | |
| http://beyond-the-seas.org/api/professor/{professor_id}/details | GET | ```{ "professor_id": "string" }``` | 200 | ```{ "professor": { "name": "string", "designation": "string", "department": "string", "research_area": [], "email": "string", "address": "string", "website": "string", "scholar_info": "string" } }``` |
