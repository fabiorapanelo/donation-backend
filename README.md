[![Build Status](https://api.travis-ci.org/fabiorapanelo/donation-backend.svg?branch=master)](https://api.travis-ci.org/fabiorapanelo/donation-backend)

# Donation Backend

****

This project is the backend layer of Doe+ App using Spring Cloud framework.

#### Authentication

Method  | Path  | Description
------------- | ------------------------- | ------------- |
POST | /login   | Generates a JWT Token to be used in 

Example:
```
Request:
POST http://localhost:8080/authentication/login
{
    "username": "foo",
    "password": "bar"
}
Response: 200 - OK
Authorization: Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhZG1pbiIsImF1dGhvcml0aWVzIjpbIlJPTEVfQURNSU4iXSwiaWF0IjoxNTQxMjUzNzEzLCJleHAiOjE1NDEzNDAxMTN9.dVuksZMwwOggMdRMTfk96k3tr4GXN4_ckXfwt_ydaZR8H2My8ol46vD_iLpG2BlAOEpPaSYK4K4MB7WeNC-aYg
```

#### Campaign

Method  | Path  | Description
------------- | ------------------------- | ------------- |
POST | /campaigns   | Create a campaign 
GET | /campaigns/search-by-user/{userId} | Get the campaigns of an user
GET | /campaigns/near-location    | Get the campaigns by location
GET | /campaigns/search-by-similar | Get the campaigns with similar name


#### Endpoints
- http://localhost:8888 - Config (Spring Cloud Config)
- http://localhost:8761 - Registry (Service Discovery with Eureka)
- http://localhost:8080 - Gateway (Netflix Zuul)
- http://localhost:8887 - Authentication (Spring Security with JWT)
- http://localhost:8881 - Campaign