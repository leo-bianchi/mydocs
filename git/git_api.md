## Intro to GitHub API

## Create remote repositories

```bash
$ curl -u 'username' https://api.github.com/user/repos -d '{"name":"repo_name"}'
```

### Parameters
|Name|Type|Description|
|----|----|-----------|
|`name`|string|**Required** Repository name|
|`description`|string|Repository description|
