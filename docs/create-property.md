# Create a property

Add a property to your portfolio.

## Before you begin

You must be a `manager` with `CRUD` access. If you don't have the access, see [Update a user information and access](/docs/update-user.md).

## Create a property

1. Open the Postman app on your desktop.

2. Create a `POST` request.

    ```
    {base_url}/properties/
    ```

3. In the **Headers** section, ensure **content-type** is `application/json`.

4. In the **Body** section, select `raw` and then enter the updated property details in the text field. The following property details are required:
    | Property name | Type | Description |
    |-------|--------|---------|
    | `id` | integer | Unique identifier of the property |
    | `building_name` |string | Name of the property |
    | `address_line_1` | string | Street name in the property's address |
    | `address_line_2` | string | Suite or apartment number of the property |
    | `address_line_3` | string | City, state, and zip code in the property's address |
    | `owner_id` | integer | Unique identifier of the owner of the property |
    | `manager_id` | integer | Unique identifier of the manager of the property |

5. Click **Send**. A property is created and it appears in the **Response Body** section.

## Example

### Request

```
{base_url}/properties
```

```json
{
    "building_name": "Ocean View Condos",
    "address_line_1": "789 Ocean View Dr",
    "address_line_2": "Suite 305",
    "address_line_3": "Atlanta, GA 35034",
    "id": 9,
    "owner_id": 7,
    "manager_id": 8
}
```

### Response

```json
{
    "building_name": "Ocean View Condos",
    "address_line_1": "789 Ocean View Dr",
    "address_line_2": "Suite 305",
    "address_line_3": "Atlanta, GA 35034",
    "id": 9,
    "owner_id": 7,
    "manager_id": 8
}
```
