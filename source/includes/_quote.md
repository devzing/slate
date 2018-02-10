# Quote

## Get or Retreive a specific Quote

```csharp
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```php
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl
  -X PUT
  -v https://<base URL>/quote
  -H "X-SwyfftApiKey: SwyfftApiKey"
  -H "Content-Type: application/json"
  -d "{\"FullAddress\": \"20 Cedar Dr, Rochelle Park NJ 07662\", \"LivingSpace\": \"1200\"}"
```

> Make sure to replace `SwyfftApiKey` with your API key.

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves the specified quote or creates a new one.

### HTTP Request

`PUT https://<base URL>/quote`

### JSON Parameters

Parameter | Required | Description
--------- | ------- | -----------
FullAddress | Yes | The full address of the home. E.g. "20 Cedar Dr, Rochelle Park NJ 07662"
LivingSpace | No | The number of square feet in the home. E.g. "1200"