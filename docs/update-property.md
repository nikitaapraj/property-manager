# Update a property

Update information about a property, such as tenant or rent.

## URL

**POST** `{base_url}/properties/{id}`

## Parameters

| Property name | Type | Required | Description |
|-------|--------|---------|---------|
| `building_type` | string | Optional | Type of the property based on its structure and use. For example, `High-rise Office`. |
| `building_name` |string | Required | Name of the property |
| `address_line_1` | string | Required | Street name in the property's address |
| `address_line_2` | string | Required | Suite or apartment number of the property. |
| `address_line_3` | string | Required | City, state, and zip code in the property's address. |
| `is_occupied` | boolean | Optional | `Y` if the property is occupied by a tenant. `N` if it's empty. |
| `tenant_name` | string | Optional | If the property is occupied, the name of the tenant. Optional if the property is unoccupied. |
| `sq_footage` | string |  Optional | Area of the property in square feet |
| `monthly_rent` | string |  Optional | Monthly rent of the property in USD |
| `id` | integer | Required | Unique identifier of the property |
| `owner_id` | integer | Required | Unique identifier of the owner of the property |
| `manager_id` | integer | Required | Unique identifier of the manager of the property |

## Example

This example changes the occupancy status of property `3` from `Y` to `N`.

### Request

```
http://localhost:3000//properties/3
```

```json
{
    "building_type": "High-rise Office",
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
    "building_type": "High-rise Office",
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
