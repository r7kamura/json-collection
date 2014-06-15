# GitHub JSON Schema
JSON Schema for GitHub API v3.

## Try API
The handy CLI HTTP Client [plz](https://github.com/r7kamura/plz)
help you try to test the API.

```sh
$ gem install plz
$ plz list_users gist name=r7kamura
$ plz list_public
$ echo '
{
  "description": "Test",
  "public": true,
  "files": {
    "hello.txt": {
      "content": "world"
    }
  }
}' > 3
$ plz create gist <3
```
