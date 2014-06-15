# GitHub API v3
* [Gist](#gist)
 * [GET /gists](#get-gists)
 * [POST /gists](#post-gists)
 * [GET /gists/:id](#get-gistsid)
 * [PATCH /gists/:id](#patch-gistsid)
 * [DELETE /gists/:id](#delete-gistsid)
 * [GET /gists/public](#get-gistspublic)
 * [GET /gists/starred](#get-gistsstarred)
 * [GET /users/:name/gists](#get-usersnamegists)
* [Commit](#commit)
 * [GET /gists/:id/commits](#get-gistsidcommits)

## Gist
Gist object

### Properties
* id - Identifier of a gist
 * Example: `"1"`
 * Type: string

### GET /gists
List the authenticated user's gists or if called anonymously, this will return all public gists

```
GET /gists HTTP/1.1
Content-Type: application/json
Host: api.github.com
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "id": "1"
}
```

### POST /gists
Create a gist

```
POST /gists HTTP/1.1
Content-Type: application/json
Host: api.github.com

{
  "id": "1"
}
```

```
HTTP/1.1 201
Content-Type: application/json

{
  "id": "1"
}
```

### GET /gists/:id
Get a single gist

```
GET /gists/:id HTTP/1.1
Content-Type: application/json
Host: api.github.com
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "id": "1"
}
```

### PATCH /gists/:id
Edit a gist

```
PATCH /gists/:id HTTP/1.1
Content-Type: application/json
Host: api.github.com

{
  "id": "1"
}
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "id": "1"
}
```

### DELETE /gists/:id
Delete a gist

```
DELETE /gists/:id HTTP/1.1
Content-Type: application/json
Host: api.github.com
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "id": "1"
}
```

### GET /gists/public
List public gists

```
GET /gists/public HTTP/1.1
Content-Type: application/json
Host: api.github.com
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "id": "1"
}
```

### GET /gists/starred
List the authenticated user’s starred gists

```
GET /gists/starred HTTP/1.1
Content-Type: application/json
Host: api.github.com
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "id": "1"
}
```

### GET /users/:name/gists
List a user's gists

```
GET /users/:name/gists HTTP/1.1
Content-Type: application/json
Host: api.github.com
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "id": "1"
}
```

## Commit


### Properties
* url - 
 * Example: `"https://api.github.com/gists/e49e8dbd1b30d170449c"`
 * Type: string
* version - 
 * Example: `"57a7f021a713b1c5a6a199b54cc514735d2d462f"`
 * Type: string
* committed_at - 
 * Example: `"2010-04-14T02:15:15Z"`
 * Type: string
 * Format: date-time

### GET /gists/:id/commits
List gist commits

```
GET /gists/:id/commits HTTP/1.1
Content-Type: application/json
Host: api.github.com
```

```
HTTP/1.1 200
Content-Type: application/json

{
  "url": "https://api.github.com/gists/e49e8dbd1b30d170449c",
  "version": "57a7f021a713b1c5a6a199b54cc514735d2d462f",
  "committed_at": "2010-04-14T02:15:15Z"
}
```

