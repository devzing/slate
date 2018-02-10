# Errors

Swyfft returns standard HTTP status codes for successful and error responses.

### HTTP status codes

Status Code | Meaning
---------- | -------
200 | Request OK
400 | Validation error
401 | Authentication errors or Unauthorized request
403 | Forbidden
500 | Swyfft server error

### Error responses

The response body for all errors includes additional error details in this format:

`{
  "StatusCode": 1104,
  "Error": {
    "Code": 1104,
    "Message": "Invalid request. Invalid LivingSpace value."
  }
}`

### Error Codes and Messages

Error Code | Meaning
---------- | -------
0 | No error.
1000 | Unknown error occurred.
1010 | Unrecognized api key.
1101 | Invalid request.
1102 | Invalid request. FullAddress is empty.
1103 | Could not find property information for specified address.
1104 | Invalid request. Invalid LivingSpace value.
1105 | Invalid request. Invalid QuoteGuid.
1201 | Sorry, we don't support this property yet. We're working on it.
1202 | Sorry, we don't cover this type of property.
1203 | A quote for this address has already been purchased.
1204 | Could not create quote. Coverage is declined.
1205 | The agent's license information is missing or does not cover this area.
1206 | Property does not appear to be a single family residence.
1301 | Failed to create quote. There is not enough data on this property to generate an automatic quote.
1401 | Your agency is over daily API call limit.
1402 | Your agency is over 5 minute API call limit.
1403 | Your agency does not have API call limits set.