---
id: zone-by-location
title: Zone by Geo location
---
##
```GET``` Zone by Geolocation

```
https://barikoi.xyz/v1/api/search/zone/API_KEY/LONGITUDE/LATITUDE
```

Returns the ward of given longitude and latitude.

## API Params

| Parameter     | Value         |
| ------------- |:-------------:| 
| longitude     | 90.418619474572   | 
| latitude      | 23.83136348674859 |

## Zone by Geolocation API Request Example

``` Js                                    
fetch('https://barikoi.xyz/v1/api/search/zone/API_KEY/90.4186194745721/23.83136348674859')
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```

## Example Response

```
[
    {
        "Zone": 1
    }
]
```