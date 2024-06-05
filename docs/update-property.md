# Update a property

Update information about a property, such as tenant or rent.

## Before you begin

* You must be a `manager` with `CRUD` access. If you don't have the access, see [Update a user information and access](/docs/update-user.md).

* Keep the property id handy.

## Update a property

1. Open the Postman app on your desktop.

2. Create a `PUT` request for the property you want to update.

    ```
    {base_url}/properties/{id}
    ```

3. In the **Headers** section, ensure **content-type** is `application/json`.

4. In the **Body** section, select `raw` and then enter the updated property details in the text field. See [Properties Reference](/docs/properties.md).
5. Click **Send**. The updated property details appear in the **Response Body** section.

## Example

### Request

This example changes the occupancy status of property `3` from `Yes` to `No`.

```
{base_url}/properties/3
```

```json
{
    "building_type": "Highrise Office",
    "building_name": "100 Park Place",
    "address_line_1": "100 Park Place Dr",
    "address_line_2": "Suite 400",
    "address_line_3": "Atlanta, GA 30303",
    "is_occupied": "N",
    "tenant_name": "Morgan & Morgan",
    "sq_footage": "10000",
    "monthly_rent": "$20000",
    "id": "1",
    "owner_id": 2,
    "manager_id": 1
}
```

### Response

```json
{
    "building_type": "Highrise Office",
    "building_name": "100 Park Place",
    "address_line_1": "100 Park Place Dr",
    "address_line_2": "Suite 400",
    "address_line_3": "Atlanta, GA 30303",
    "is_occupied": "N",
    "tenant_name": "Morgan & Morgan",
    "sq_footage": "10000",
    "monthly_rent": "$20000",
    "id": "1",
    "owner_id": 2,
    "manager_id": 1
}
```
