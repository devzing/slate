# Address

```csharp
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```php
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
curl
  -X GET
  -v https://<base URL>/addresses?partialAddress=2300%20ha
  -H "X-SwyfftApiKey: SwyfftApiKey"
  -H "Content-Type: application/json"
```

> Make sure to replace `SwyfftApiKey` with your API key.

> The above command returns JSON structured like this:

```json
{
   "Addresses":[
      {
         "AddressKey":"60201214600",
         "Street1":"2300 Harrison St",
         "City":"Evanston",
         "State":"IL",
         "Zip5":"60201",
         "FullAddress":"2300 Harrison St, Evanston IL 60201"
      },
      {
         "AddressKey":"36617251500",
         "Street1":"2300 Hathcox St",
         "City":"Mobile",
         "State":"AL",
         "Zip5":"36617",
         "FullAddress":"2300 Hathcox St, Mobile AL 36617"
      }
   ],
   "StatusCode":0,
   "Error":null
}
```

This endpoint retrieves addresses formatted in a manner that Swyfft recognizes.

### HTTP Request

`GET https://<base URL>/address?partialAddress=<partial address>`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
partialAddress | Yes | A partial address for the home. E.g. "2300%20ha" - remember to urlencode the value. The system does a "starts with" comparison so trying to seach for a town name will not work.
