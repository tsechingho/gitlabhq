# Gitlab API

All API requests require authentication. You need to pass `private_token` parameter to authenticate.

To get or reset your token visit your profile.

If no or invalid `private_token` provided error message will be returned with status code 401:

```json
{
  "message": "401 Unauthorized"
}
```

API requests should be prefixed with `api` and the API version.
API version is equal to Gitlab major version number and defined in `lib/api.rb`.

Example of valid API request:

```
GET http://example.com/api/v2/projects?private_token=QVy1PB7sTxfy4pqfZM1U
```

The API uses JSON to serialize data. You don't need to specify `.json` at the end of API URL.

#### Pagination

When listing resources you can pass the following parameters:

+ `page` (default: `1`) - page number
+ `per_page` (default: `20`, max: `100`) - how many items to list per page

## Contents

+ [Users](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/users.md)
+ [Projects](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/projects.md)
+ [Snippets](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/snippets.md)
+ [Issues](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/issues.md)
+ [Milestones](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/milestones.md)
