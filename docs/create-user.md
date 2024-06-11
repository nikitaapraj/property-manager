# Create a user

Create an `owner` or `manager` user and assign them permissions.

## URL

**POST** `{base_url}/users/`

## Parameters

| Property name | Type | Required | Description |
|-------|--------|---------|---------|
| `id` | integer |Required| Unique identifier of the user |
| `username` | string | Required | Unique alphanumeric username of the user. Minimum length 6 characters. Maximum length 10 characters. Cannot include special characters. |
| `role` | string | Required | Relation of the user with the property. Can be either `manager` or `owner`. |
| `permissions` | string | Required |Access level of the user. A `manager` must have the `crud` access. An `owner` must have the `read-only` access. |

## Example

### Request

```
http://localhost:3000/users/
```

```json
{
    "id": "4",
    "username": "patrick.johnson",
    "role": "manager",
    "permissions": "crud"
}
```

### Response

```json
{
    "id": "4",
    "username": "patrick.johnson",
    "role": "manager",
    "permissions": "crud"
}
```
