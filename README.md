# ml-api



## Usage


* All responses will have the form

```json
{
	"data": "",
	"message": "",
}
```



## List ALL Digits


### Definition
* `GET /digits`


### Response
* `200 OK` on success
```json
	[
		{
			"identifier": "2123",
			"name": "3",
		},
		{
			"identifier": "4732",
			"name": "9"
		}
	]
```



## Add a New Digit


### Definition
`POST /digits`


### Arguments
* `"identifier":string`: a globally unique identifier for this digit
* `"name":`: name this digit eg. 0-9
<br/><br/>If a device with the given identifier already exists, the existing device will be overwritten


### Response
```json
{
	"identifier": "3829",
	"name": "6"
}
```



## Lookup Devices Details


## Definition
`GET /device/<identifier>`

## Response
* `404 Not Found` if the identifier does not exist
* `200 OK` on success

```json
{
	"identifier": "3829",
	"name": "6"
}
```



## Delete a Digit


## Definition
`DELETE /digits/<identifier>`

## Response
* `404 Not Found` if the identifier does not exist
* `204 No Content` on success