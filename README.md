# Hooligram Documentation

## Protocol V2

### Verification

#### Code request

Client request

```json
{
  "payload": {
    "country_code": "<string>",
    "phone_number": "<string>"
  },
  "type": "VERIFICATION_REQUEST_CODE_REQUEST"
}
```

Server success response

```json
{
  "payload": {
  },
  "type": "VERIFICATION_REQUEST_CODE_SUCCESS"
}
```

Server failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "VERIFICATION_REQUEST_CODE_FAILURE"
}
```

#### Code submit

Client request

```json
{
  "payload": {
    "verification_code": "<string>"
  },
  "type": "VERIFICATION_SUBMIT_CODE_REQUEST"
}
```

Server success response

```json
{
  "payload": {
  },
  "type": "VERIFICATION_SUBMIT_CODE_SUCCESS"
}
```

Server failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "VERIFICATION_SUBMIT_CODE_FAILURE"
}
```
