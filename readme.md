This repo is a response for one of [json-server questions](https://github.com/typicode/json-server/issues/417)

## running the exampl
```sh
git clone https://github.com/Nilegfx/json-server-answer-417.git

cd json-server-answer-417

npm install

node server
```

### make a request with basic authentication
from your command line, run 
```sh
curl -u yourusername:yourpassword http://localhost:3000/posts
```
**responses with status 200:**
```json
{
  "user": "yourusername",
  "body": [
    {
      "id": 1,
      "title": "first post title",
      "name": "ahmed ayoub"
    }
  ]
}
```
### a request **without** basic authentication
from your command line, run 
```sh
curl http://localhost:3000/posts
```

***responses with status 401:***
```json
{
  "error": "unauthorized"
}
```