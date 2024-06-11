# Get a user

Find a user by their user id.

## URL

**GET** `{base_url}/users/{id}`

### Parameters

`id`: Integer. Unique identifier of the user.

## Example

### Request

```
http://localhost:3000//users/2
```

### Response

```
{
    "id": 2,
    "username": "sam.jones",
    "role": "owner",
    "permissions": "read-only"
}
```
