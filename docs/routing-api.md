---
id: route-api
title: Routing Api
---
##
```GET``` Routing
```
https://barikoi.xyz/v1/api/route/API_KEY/90.362548828125,23.94107556246209;90.31585693359375,24.134221690669204?overview=true&alternatives=true&steps=true&hints=
```

This api provides routing details for two location points.

## FormData Key and Value

| Parameter     | Value         |
| ------------- |:-------------:| 
| overview      | true          |
| alternatives  | true          | 
| steps         | true          |
| hints         |    ;          |

## Routing API Request Example

``` Js
<code class="code-snippet" id="api-routing-example">
fetch('https://barikoi.xyz/v1/api/route/API_KEY/90.362548828125,23.94107556246209;90.31585693359375,24.134221690669204?overview=true&alternatives=true&steps=true&hints=')
.then(response => response.json())
.catch(error => console.error('Error:', error))
.then(response => console.log('Success:', response))
</code>
```

## Example Response

```
{
    "code": "Ok",
    "routes": [
        {
            "geometry": "g}bqCmhpfPjf@uE_P_~BueAjZ}sDpCg@~t@_{DdfF}ZbrCodA`bCsM{m@ojCaUw^meAmg@eS_~A_Ok}AbFmXbQoi@mmAuxEfS",
            "legs": [
                {
                    "steps": [],
                    "distance": 33452.2,
                    "duration": 2481.4,
                    "summary": "",
                    "weight": 2481.4
                }
            ],
            "distance": 33452.2,
            "duration": 2481.4,
            "weight_name": "routability",
            "weight": 2481.4
        }
    ],
    "waypoints": [
        {
            "hint": "V10DgFldA4AAAAAAJwAAAAAAAAAfAQAAAAAAAFZN10EAAAAA6SFHQwAAAAAnAAAAAAAAAB8BAACEAAAA6tliBeZObQG10mIF1E9tAQAATwvGEH3j",
            "distance": 189.684241,
            "name": "",
            "location": [
                90.364394,
                23.940838
            ]
        },
        {
            "hint": "xy0BgPzPAoBDAAAAKwAAAL8QAAAtBgAAjQGVQqNFPkI1VJRFXcnaREMAAAArAAAAvxAAAC0GAACEAAAAsjtiBbBHcAFRHGIFTkJwATMAnwrGEH3j",
            "distance": 830.734383,
            "name": "Mouchak - Fulbari Road",
            "location": [
                90.32389,
                24.1356
            ]
        }
    ]
}
```