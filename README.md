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

### Usage
```sh
$ plz --help
Usage: plz <action> <target> [headers|params] [options]
    -h, --help                    Display help message
        --no-color                Disable coloring output
        --no-response-body        Hide response body
        --no-response-header      Hide response header
Examples:
  plz show gist id=1
  plz list gist
  plz list_starred gist
  plz list_users gist name=r7kamura
  plz list_public gist
  plz create gist
  plz update gist id=1
  plz delete gist id=1
  plz list_commits gist id=1
  plz star gist id=1
  plz unstar gist id=1
  plz starred gist id=1
  plz fork gist id=1
```
