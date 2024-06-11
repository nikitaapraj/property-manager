# `/users`

## Endpoint

`{base_url}/users`

Contains information about a user. A user can be either an owner or manager of a real estate property.

## Example

```json
{
    "id": 1,
    "username": "jane.smith",
    "role": "manager",
    "permissions": "crud"
}
```

## Properties

| Property name | Type | Required | Description |
|-------|--------|---------|---------|
| `id` | integer |Required| Unique identifier of the user |
| `username` | string | Required | Unique alphanumeric username of the user. Minimum length 6 characters. Maximum length 10 characters. Cannot include special characters. |
| `role` | string | Required | Relation of the user with the property. Can be either `manager` or `owner`. |
| `permissions` | string | Required |Access level of the user. A `manager` must have the `crud` access. An `owner` must have the `read-only` access. |

## Operations

* [Create a user](/create-user.md)
* [Find a user](/get-user.md)
* [Update a user information and access](/update-user.md)
* [Delete a user](/delete-user.md)