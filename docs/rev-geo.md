---
id: rev-geo
title: Reverse Geocode
---
##
```GET``` Reverse Geocoding API

```
https://barikoi.xyz/v1/api/search/reverse/API_KEY/geocode?longitude=90.3737&latitude=23.7881&district=true&post_code=true&country=true&sub_district=true&union=false&pauroshova=false&location_type=true
```
Returns an address given longitude and latitude.

## API PARAMS

| Parameter     | Value         |
| ------------- |:-------------:| 
| longitude     | 90.3737       |
| latitude      | 23.7881       |
| district      | true       |
| post_code     | true       |
| country       | true       |
| sub_district  | true       |
| union         | false       |
| pauroshova    | false       |
| location_type | true       |


## Reverse Geocoding API Request Example

``` Js                            
fetch('https://barikoi.xyz/v1/api/search/reverse/API_KEY/geocode?longitude=90.3737&latitude=23.7881&district=true&post_code=true&country=true&sub_district=true&union=false&pauroshova=false&location_type=true')
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```

## Example Response

```
{
    "place": {
        "id": 177936,
        "distance_within_meters": 1.167,
        "address": "Mohosin Uddin, House 462, West Shewrapara",
        "area": "Mirpur",
        "city": "Dhaka",
        "postCode": 1216,
        "location_type": "Urban",
        "district": "Dhaka",
        "country": "Bangladesh",
        "sub_district": "Kafrul"
    },
    "status": 200
}
```