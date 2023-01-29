# Postman
Registration:

Curl:
curl -X 'POST' \
  'https://api.realworld.io/api/users' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "user": {
    "username": "DinaAs",
    "email": "didi@gmail.com",
    "password": "didi1212"
  }
}'
	
Response body: 
{
  "user": {
    "email": "didi@gmail.com",
    "username": "DinaAs",
    "bio": null,
    "image": "https://api.realworld.io/images/smiley-cyrus.jpeg",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImRpZGlAZ21haWwuY29tIiwidXNlcm5hbWUiOiJEaW5hQXMiLCJpYXQiOjE2NzUwMDYwNzksImV4cCI6MTY4MDE5MDA3OX0.Hqt9o5DyMqbTcy7cuytVJBcDdS07jftIyeEOEdxJn4A"
  }
}

Authentication:
Curl: 
curl -X 'POST' \
  'https://api.realworld.io/api/users/login' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "user": {
    "email": "didi@gmail.com",
    "password": "didi1212"
  }
}'

	
Response body:
{
  "user": {
    "email": "didi@gmail.com",
    "username": "DinaAs",
    "bio": null,
    "image": "https://api.realworld.io/images/smiley-cyrus.jpeg",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImRpZGlAZ21haWwuY29tIiwidXNlcm5hbWUiOiJEaW5hQXMiLCJpYXQiOjE2NzUwMDYxMjIsImV4cCI6MTY4MDE5MDEyMn0.rsKykPjqim_0LxtwhInfbaCBzJSwE4MxLHGYo1rjzeQ"
  }
}

Get Current User:
Curl: 
curl -X 'GET' \
  'https://api.realworld.io/api/user' \
  -H 'accept: application/json'
  
 	
Error: response status is 401
Response body:
{
  "status": "error",
  "message": "missing authorization credentials"
}

