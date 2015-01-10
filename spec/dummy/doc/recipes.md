## GET /recipes/:id
Returns the recipe.

### Example

#### Request
```
GET /recipes/1 HTTP/1.1
Content-Length: 0
Content-Type: application/json
Host: example.org
```

#### Response
```
HTTP/1.1 200
Cache-Control: max-age=0, private, must-revalidate
Content-Length: 111
Content-Type: application/json; charset=utf-8
ETag: "2dbe8120a13a69e6463d199e5aad8cff"
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
X-Request-Id: 32cb21ea-37e1-4f86-90bc-c2412374e051
X-Runtime: 0.009890
X-XSS-Protection: 1; mode=block

{
  "id": 1,
  "name": "test",
  "type": 2,
  "created_at": "2015-01-10T23:41:43.384Z",
  "updated_at": "2015-01-10T23:41:43.384Z"
}
```

## POST /recipes
Creates
a
new
recipe!


### Parameters
* `name` string (required, except: `["alice", "bob"]`)
* `type` integer (only: `1..3`)

### Example

#### Request
```
POST /recipes HTTP/1.1
Accept: application/json
Content-Length: 24
Content-Type: application/json
Host: www.example.com

{
  "name": "name",
  "type": 1
}
```

#### Response
```
HTTP/1.1 201
Cache-Control: max-age=0, private, must-revalidate
Content-Length: 111
Content-Type: application/json; charset=utf-8
ETag: "6e86c34de89deadb2d38f085abe4c828"
Location: http://www.example.com/recipes/1
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
X-Request-Id: 66010a4a-bbc0-40f4-8c9c-4db6c29a2f29
X-Runtime: 0.006379
X-XSS-Protection: 1; mode=block

{
  "id": 1,
  "name": "name",
  "type": 1,
  "created_at": "2015-01-10T23:41:43.466Z",
  "updated_at": "2015-01-10T23:41:43.466Z"
}
```
