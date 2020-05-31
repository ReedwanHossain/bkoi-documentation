---
id: geo-server
title:Reverse Geocoding (Server)
---

##
```GET``` Reverse Geocoding Server API

```
https://barikoi.xyz/v1/api/search/reverse/API_KEY/geocode?longitude=TARGET_LONGITUDE&latitude=TARGET_LATITUDE
```
Returns an address given longitude and latitude.

## API PARAMS

| Parameter     | Value         |
| ------------- |:-------------:| 
| longitude     | 90.3666       |
| latitude      | 23.8372       |

## Rate limit

2000 Request per minute

## Reverse Geocoding Server API Request Example

``` Js                                    
fetch('https://barikoi.xyz/v1/api/search/reverse/API_KEY/geocode?longitude=90.3666&latitude=23.8372')
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```

## Example Response

```
{
    "place": {
        "id": 452923,
        "distance_within_meters": 10.544959558542,
        "address": "Artland, Jol Torongo, House 555, Road 9",
        "area": "Mirpur Dohs",
        "city": "Dhaka"
    },
    "status": 200
}      
```