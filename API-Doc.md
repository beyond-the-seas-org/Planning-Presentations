# API Documentation

<!-- create tables for api documentation -->

## Authentication

| API Endpoint | HTTP Method | Request Body | Response Code | Response Body |
| --- | --- | --- | --- | --- |
| ```POST``` Login | | | | |
| beyond-the-seas.org/login/ | POST | ```{ "username": "asif", "password": "codeword" }``` | 200 | ```{ "token": "string" }``` |
| ```GET``` Logout | | | | |
| beyond-the-seas.org/logout/ | GET | | 200 | |


## User Profile
<!-- API endpoint format: beyond-the-seas.org/api/user/ -->
<!-- Beutify the response body so that it looks like JSON format -->

| API Endpoint | HTTP Method | Request Body | Response Code | Response Body |
| --- | --- | --- | --- | --- |
| ```POST``` Create User | | | | |
| beyond-the-seas.org/api/user/create | POST | ```{ "username": "asif", "password": "codeword", "email": "asif@gmail.com", "first_name": "Asif", "last_name": "Haider", "gender": "male", "age": "23"}``` | 201 | ``` { "profile": {} } ``` |
| ```POST``` Update User Profile | | | | |
| beyond-the-seas.org/api/user/{user_id}/update-profile | POST | ``` { "user_id": 1, "bsc-varsity": "BUET", "bsc-year": "2024", "msc-varsity": "BUET", "msc-year": "2026", "bsc-cgpa": "3.80", "msc-cgpa": "3.90", "gre-score": ["155", "165", "4.0"], "language-score": ["23", "24", "25", "27"], "github-link": "github.com/asifhaider", "linkedin-link": "linkedin.com/asifhaider", "personal-site": "asifhaider.github.io", "publication-link": ["link1", "link2"] } ``` | 200 | ``` { "profile": {} } ``` |
| ```GET``` User Profile | | | | |
| beyond-the-seas.org/api/user/{user_id}/profile | GET | ```{ "user_id": 1 }``` | 200 | ```{ "profile": {} }``` |

## Professor
<!-- API endpoint format: beyond-the-seas.org/api/professor/ -->

| API Endpoint | HTTP Method | Request Body | Response Code | Response Body |
| --- | --- | --- | --- | --- |
| ```GET``` Search Professor | | | | |
beyond-the-seas.org/api/professor/search?start=0&count=10 | GET | ```{ "keyword": "Big Data" }``` | 200 | ```{ "professors": [] }``` |
| ```GET``` Professor Details | | | | |
| beyond-the-seas.org/api/professor/{professor_id}/details | GET | ```{ "professor_id": 3 }``` | 200 | ```{ "professor": {"name": "Latifur Khan", "designation": "Professor", "department": "Computer Science", "university": "University of Texas at Dallas", "research-area": ["Big Data", "Data Streams", "Cyber Security"], "email": "khan@utdallas.edu", "address": "3322 ECSS, Dallas, TX, USA", "website": "https://cs.utdallas.edu/people/faculty/khan-latifur/", "scholar-info": ["14004", "65"], "funding-opportunity": [], "ongoing-projects": [], "feedback": []}``` |

