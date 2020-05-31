---
id: autocomplete
title: Autocomplete
---

## Method
```GET``` Autocomplete API

## URL
```
https://barikoi.xyz/v1/api/search/autocomplete/API_KEY/place?q=shopno&latitude=23.873751&longitude=90.396454
```
Barikoi Autocomplete. Returns a place's id, longitude, latitude, address, city, area, postCode, pType & uCode

## API Params

| Parameter     | Value         |
| ------------- |:-------------:| 
| q             | shopno   | 
| longitude     | 90.3964       |
| latitude      | 23.8737       |

```Here, Latitude and Longitude are optional Parameters.When Latitude and Longitude are provided in the request Parameter then the search result is returned based on the provided longitude latitude.```

## API Request Example

```Js
fetch("https://barikoi.xyz/v1/api/search/autocomplete/API_KEY/place?q=shopno&latitude=23.873751&longitude=90.396454")
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```

## Example Response
```
{
   "places":[
      {
         "area":"Uttara",
         "uCode":"MWPO8698",
         "address":"Shopno Neer, House 15, Gausul Azam Avenue, Sector 14",
         "city":"Dhaka",
         "latitude":"23.869151117076033",
         "pType":"Residential",
         "postCode":1230,
         "id":205216,
         "longitude":"90.39050549268723"
      },
      {
         "area":"Uttara",
         "uCode":"EQAI5125",
         "address":"Shopno Neer, House 49, Road 13, Sector 13",
         "city":"Dhaka",
         "latitude":"23.873195116043306",
         "pType":"Residential",
         "postCode":1230,
         "id":211017,
         "longitude":"90.38691200315951"
      },
      {
         "area":"Uttara",
         "uCode":"AUTH9999",
         "address":"Shopno Chhowa Ladies Tailors, House 14, Road 7\/A, Sector 3",
         "city":"Dhaka",
         "latitude":"23.86523106661817",
         "pType":"Shop",
         "postCode":1230,
         "id":19584,
         "longitude":"90.39408891592521"
      }
      ........
    ],
    "status":200
    }
```

To get post office autocomplete just add post_office param to request body with the value true

## Post Office Autocomplete API
```
https://barikoi.xyz/v1/api/search/autocomplete/API_KEY/place?q=Mirpur&post_office=true
```
Barikoi Autocomplete. Returns a place's id, longitude, latitude, address, city, area, postCode, pType & uCode

## API Params

| Parameter     | Value         |
| ------------- |:-------------:| 
| q             | Mirpur        |
| post_office   | true          | 

## Autocomplete API Request Example

``` Js
fetch("https://barikoi.xyz/v1/api/search/autocomplete/API_KEY/place?q='Jol Torongo'")
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```
## Example Response
```
{
    "places": [
        {
            "id": 4,
            "latitude": "23.811978035351842",
            "longitude": "90.34750800579786",
            "address": "Chiriyakhana Post Office, Zoo Road, Section 1",
            "city": "Dhaka",
            "area": "Mirpur",
            "postCode": 1216,
            "pType": "Government",
            "uCode": "WEST4687"
        },
        {
            "id": 5,
            "latitude": "23.80330755057738",
            "longitude": "90.36122918128967",
            "address": "Mirpur Post Office, Main Road, Section 2, Mirpur 2",
            "city": "Dhaka",
            "area": "Mirpur",
            "postCode": 1216,
            "pType": "Government",
            "uCode": "BAND7192"
        },
        {
            "id": 6,
            "latitude": "23.820675852230316",
            "longitude": "90.3647304698825",
            "address": "Pallabi Post Office, Begum Rokeya Sarani, Purobi",
            "city": "Dhaka",
            "area": "Mirpur",
            "postCode": 1216,
            "pType": "Government",
            "uCode": "ALSO4104"
        }
    ],
    "status": 200
}                    
```