---
id: nearby
title: Nearby
---
## 
```GET``` Nearby API

```
https://barikoi.xyz/v1/api/search/nearby/API_KEY/DISTANCE/LIMIT?longitude=TARGET_LONGITUDE&latitude=TARGET_LATITUDE
```
All Nearby API counts according to the limit parameter or number of places returned in response data

## API PARAMS

| Parameter     | Value         |
| ------------- |:-------------:| 
| longitude     | 90.36668110638857     |
| latitude      | 28.83723803415923     | 
| distance      | 0.5 (km)      |
| limit         | 10            | 

## Nearby API Request Example

``` Js
fetch('https://barikoi.xyz/v1/api/search/nearby/API_KEY/0.5/10?longitude=90.36668110638857&latitude=23.83723803415923')
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```
## Example Response
```
{
    "Place": [
        {
            "id": 452923,
            "name": "Artland",
            "distance_in_meters": 0,
            "longitude": "90.36668110638857",
            "latitude": "23.83723803415923",
            "pType": "Education",
            "address": "Artland, Jol Torongo, House 555, Road 9",
            "area": "Mirpur Dohs",
            "city": "Dhaka",
            "postCode": 1216,
            "subType": "Art School",
            "uCode": "IDIX1880",
            "ST_AsText(location)": "POINT(90.36668110638857 23.83723803415923)"
        },
        {
            "id": 485763,
            "name": "Mulytic Labs",
            "distance_in_meters": 11.246276012918,
            "longitude": "90.36672234535217",
            "latitude": "23.837144191228138",
            "pType": "Office",
            "address": "Mulytic Labs, Jol Torongo, House 555, Road 9",
            "area": "Mirpur Dohs",
            "city": "Dhaka",
            "postCode": 1216,
            "subType": "Branch Office",
            "uCode": "IDVH3378",
            "ST_AsText(location)": "POINT(90.36672234535217 23.837144191228138)"
        }
        ........
    ]
}                 
```

##
``` GET``` Nearby API with Category

```
https://barikoi.xyz/v1/api/search/nearby/category/API_KEY/DISTANCE/LIMIT?longitude=TARGET_LONGITUDE&latitude=TARGET_LATITUDE&ptype=CATEGORY
```
This returns data with specific [place type](https://barikoi.com/supported_place_types)

## API PARAMS

| Parameter     | Value         |
| ------------- |:-------------:| 
| longitude     | 90.36668110638857    |
| latitude      | 28.83723803415923     | 
| ptype         | Office        |
| distance      | 1 (km)        |
| limit         | 10            |

## Nearby API with Category Request Example

```Js
fetch('https://barikoi.xyz/v1/api/search/nearby/category/API_KEY/1/10?longitude=90.36668110638857&&latitude=23.83723803415923&ptype=office')
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```
## Example Response

```
{
    "Place": [
        {
            "id": 485763,
            "name": "Mulytic Labs",
            "distance_in_meters": 11.246276012918,
            "longitude": "90.36672234535217",
            "latitude": "23.837144191228138",
            "address": "Mulytic Labs, Jol Torongo, House 555, Road 9",
            "city": "Dhaka",
            "area": "Mirpur Dohs",
            "pType": "Office",
            "subType": "Branch Office",
            "uCode": "IDVH3378",
            "contact_person_phone": "+880-131-848-54",
            "ST_AsText(location)": "POINT(90.36672234535217 23.837144191228138)"
        },
        {
            "id": 415887,
            "name": "Acme Technologies Ltd.",
            "distance_in_meters": 66.847925555348,
            "longitude": "90.36731514526763",
            "latitude": "23.837396371230316",
            "address": "Acme Technologies Ltd., House 630, Road 9",
            "city": "Dhaka",
            "area": "Mirpur Dohs",
            "pType": "Office",
            "subType": "HEAD OFFICE",
            "uCode": "QMVA4960",
            "contact_person_phone": null,
            "ST_AsText(location)": "POINT(90.36731514526763 23.837396371230316)"
        },
        {
            "id": 465845,
            "name": "Square Feet Housing Limited",
            "distance_in_meters": 72.221686161082,
            "longitude": "90.36676794290543",
            "latitude": "23.837882665791582",
            "address": "Square Feet Housing Limited, House 704, Road 10",
            "city": "Dhaka",
            "area": "Mirpur Dohs",
            "pType": "Office",
            "subType": "Office",
            "uCode": "JBUI0060",
            "contact_person_phone": null,
            "ST_AsText(location)": "POINT(90.36676794290543 23.837882665791582)"
        }
        .......
    ]
}                  
```

##
```GET``` Nearby API with Multiple Types

```
https://barikoi.xyz/v1/api/search/nearby/multi/type/API_KEY/DISTANCE/LIMIT?q=PLACE_TYPES&longitude=TARGET_LONGITUDE&latitude=TARGET_LATITUDE
```
This returns data with specific [place types](https://barikoi.com/supported_place_types)

## API PARAMS

| Parameter     | Value         |
| ------------- |:-------------:| 
| longitude     | 90.36668110638857    |
| latitude      | 28.83723803415923     | 
| q             | atm,school    |
| distance      | 5 (km)        |
| limit         | 5             |

## Nearby API with Multiple Types Request Example

``` Js
fetch('https://barikoi.xyz/v1/api/search/nearby/multi/type/API_KEY/5/5?q=atm,school&longitude=90.41634254157543&latitude=23.832393074088362')
    .then(response => response.json())
    .catch(error => console.error('Error:', error))
    .then(response => console.log('Success:', response))
```
## Example Response

```
{
    "Places": [
        {
            "id": 97640,
            "name": "Islami Bank Khilkhet (IBBL)",
            "distance_in_meters": 433.44554955804,
            "longitude": "90.41691217571498",
            "latitude": "23.828529979666975",
            "pType": "Bank",
            "address": "Islami Bank Khilkhet (IBBL), House 32, Road 1, Nikunja 2",
            "area": "Nikunja",
            "city": "Dhaka",
            "postCode": 1229,
            "subType": "Bank Branch",
            "uCode": "BING7101",
            "ST_AsText(location)": "POINT(90.41691217571498 23.828529979666975)"
        },
        {
            "id": 392429,
            "name": "Uttara Bank Khilkhet",
            "distance_in_meters": 436.92065060675,
            "longitude": "90.41892282664776",
            "latitude": "23.829251635052586",
            "pType": "Bank",
            "address": "Uttara Bank Khilkhet, House 2/a, Road 02, Nikunja 2",
            "area": "Nikunja",
            "city": "Dhaka",
            "postCode": 1229,
            "subType": "Bank Branch",
            "uCode": "MUAF7035",
            "ST_AsText(location)": "POINT(90.41892282664776 23.829251635052586)"
        },
        {
            "id": 488667,
            "name": "Ajij Co Operative Commerce & Finance Bank Limited (Accf)",
            "distance_in_meters": 574.2087513775,
            "longitude": "90.4209088075678",
            "latitude": "23.829356648068174",
            "pType": "Bank",
            "address": "Ajij Co Operative Commerce & Finance Bank Limited (Accf), House B-25, Khilkhet Bazar",
            "area": "Khilkhet",
            "city": "Dhaka",
            "postCode": 1229,
            "subType": "Bank Branch",
            "uCode": "AHIJ6882",
            "ST_AsText(location)": "POINT(90.4209088075678 23.829356648068174)"
        }
        .......
    ]
}                           
```
