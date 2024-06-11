# Create a property

Add a property to your portfolio.

## URL

**POST** `{base_url}/properties/`

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

### Request

`http://localhost:3000//properties`

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
