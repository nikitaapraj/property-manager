# Update a user

Update information about a user, such as change manager to owner or vice versa.

## URL

**POST** `{base_url}/users/{id}`

## Parameters

| Property name | Type | Required | Description |
|-------|--------|---------|---------|
| `role` | string | Required | Relation of the user with the property. Can be either `manager` or `owner`. |
| `permissions` | string | Required | Access level of the user. A `manager` must have the `crud` access. An `owner` must have the `read-only` access. |

*Note*:
A user's `username` and `id` are not changeable. If you want to change these values, create a new user and update the property assignments for them. Then delete the old user.

## Example

This example changes the role of user `3` from `manager` to `owner` and permissions from `crud` to `read-only`.

### Request

```
http://localhost:3000/user/3
```

```json
{
    "id": 3,
    "username": "christie.williams",
    "role": "manager",
    "permissions": "crud"
}
```

### Response

```json
{
    "id": 3,
    "username": "christie.williams",
    "role": "owner",
    "permissions": "read-only"
}
```
