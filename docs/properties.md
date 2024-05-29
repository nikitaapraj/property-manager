# `/properties`

## Endpoint

`{base_url}/properties`

Contains information about a real estate property.

## Example

```json
{
    "building_type": "Highrise Office",
    "building_name": "100 Park Place",
    "address_line_1": "100 Park Place Dr",
    "address_line_2": "Suite 400",
    "address_line_3": "Atlanta, GA 30303",
    "is_occupied": "Y",
    "tenant_name": "Morgan & Morgan",
    "sq_footage": "10000",
    "monthly_rent": "$20000",
    "id": 1,
    "owner_id": 2,
    "manager_id": 1
}
```

## Properties

| Property name | Type | Description 
| --- | ---- | --- 
| `building_type` | string | Type of the property based on its structure and use. For example, `Highrise Office`.
| `building_name` |string | Name of the property
| `address_line_1` | string | Street name in the property's address 
| `address_line_2` | string | Optional. Suite or apartment number of the property.
| `address_line_3` | string | City, state, and zip code in the property's address.
| `is_occupied` | boolean | `Y` if the property is occupied by a tenant. `N` if it's empty.
| `tenant_name` | string | If the property is occupied, the name of the tenant. Optional if the property is unoccupied.
| `sq_footage` | string | Area of the property in suqare feet
| `monthly_rent` | string | Monthly rent of the property in USD
| `id` | integer | Unique identifier of the property
| `owner_id` | integer | Unique identifier of the owner of the property
| `manager_id` | integer | Unique identifier of the manager of the property
---

## Operations

* [Create a property](/docs/create-property.md)
* [Find a property](/docs/get-property.md)
* [Update a property](/docs/update-property.md)
* [Delete a property](/docs/delete-property.md)