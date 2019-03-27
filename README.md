# Hooligram Documentation

## Protocol V2

### Verification

#### Code request

Client request

```json
{
  "id": "<string>",
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
  "id": "<string>",
  "payload": {
  },
  "type": "VERIFICATION_REQUEST_CODE_SUCCESS"
}
```

Server failure response

```json
{
  "id": "<string>",
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
  "id": "<string>",
  "payload": {
    "verification_code": "<string>"
  },
  "type": "VERIFICATION_SUBMIT_CODE_REQUEST"
}
```

Server success response

```json
{
  "id": "<string>",
  "payload": {
  },
  "type": "VERIFICATION_SUBMIT_CODE_SUCCESS"
}
```

Server failure response

```json
{
  "id": "<string>",
  "payload": {
    "errors": ["<string>"]
  },
  "type": "VERIFICATION_SUBMIT_CODE_FAILURE"
}
```

### Authorization

#### Sign in

Client request

```json
{
  "id": "<string>",
  "payload": {
    "country_code": "<string>",
    "phone_number": "<string>",
    "verification_code": "<string>"
  },
  "type": "AUTHORIZATION_SIGN_IN_REQUEST"
}
```

Server success response

```json
{
  "id": "<string>",
  "payload": {
  },
  "type": "AUTHORIZATION_SIGN_IN_SUCCESS"
}
```

```json
{
  "id": "<string>",
  "payload": {
    "errors": ["<string>"]
  },
  "type": "AUTHORIZATION_SIGN_IN_FAILURE"
}
```

### Message group

#### Create message group

Client request

```json
{
  "id": "<string>",
  "payload": {
    "group_name": "<string>",
    "member_sids": ["<string>"]
  },
  "type": "GROUP_CREATE_REQUEST"
}
```

Server success response

```json
{
  "id": "<string>",
  "payload": {
    "message_group_id": "<int>"
  },
  "type": "GROUP_CREATE_SUCCESS"
}
```

Server failure response

```json
{
  "id": "<string>",
  "payload": {
    "errors": ["<string>"]
  },
  "type": "GROUP_CREATE_FAILURE"
}
```
