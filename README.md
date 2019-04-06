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

### Authorization

#### Sign in

Client request

```json
{
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
  "payload": {
  },
  "type": "AUTHORIZATION_SIGN_IN_SUCCESS"
}
```

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "AUTHORIZATION_SIGN_IN_FAILURE"
}
```

### Group

#### Create group

Client request

```json
{
  "payload": {
    "action_id": "<string>",
    "group_name": "<string>",
    "member_sids": ["<string>"]
  },
  "type": "GROUP_CREATE_REQUEST"
}
```

Server success response

```json
{
  "payload": {
    "action_id": "<string>",
    "group_id": "<int>"
  },
  "type": "GROUP_CREATE_SUCCESS"
}
```

Server failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "GROUP_CREATE_FAILURE"
}
```

#### Leave group

Client request

```json
{
  "payload": {
    "group_id": "<int>"
  },
  "type": "GROUP_LEAVE_REQUEST"
}
```

Server success response

```json
{
  "payload": {
  },
  "type": "GROUP_LEAVE_SUCCESS"
}
```

Server failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "GROUP_LEAVE_FAILURE"
}
```

#### Add new member

Client request

```json
{
  "payload": {
    "group_id": "<int>",
    "member_sid": "<string>"
  },
  "type": "GROUP_ADD_MEMBER_REQUEST"
}
```

Server success response

```json
{
  "payload": {
  },
  "type": "GROUP_ADD_MEMBER_SUCCESS"
}
```

Server failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "GROUP_ADD_MEMBER_FAILURE"
}
```

#### Group update

Server request

```json
{
  "payload": {
    "date_created": "<string>",
    "group_id": "<int>",
    "group_name": "<string>",
    "member_sids": ["<string>"]
  },
  "type": "GROUP_DELIVER_REQUEST"
}
```

Client success response

```json
{
  "payload": {
    "group_id": "<int>"
  },
  "type": "GROUP_DELIVER_SUCCESS"
}
```

Client failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "GROUP_DELIVER_FAILURE"
}
```

### Messaging

#### Send message

Client request

```json
{
  "payload": {
    "action_id": "<string>",
    "group_id": "<int>",
    "content": "<string>"
  },
  "type": "MESSAGING_SEND_REQUEST"
}
```

Server success response

```json
{
  "payload": {
    "action_id": "<string>",
    "message_id": "<int>"
  },
  "type": "MESSAGING_SEND_SUCCESS"
}
```

Server failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "MESSAGING_SEND_FAILURE"
}
```

#### Message update

Server request

```json
{
  "payload": {
    "content": "<string>",
    "date_created": "<string>",
    "group_id": "<int>",
    "message_id": "<int>",
    "sender_sid": "<string>"
  },
  "type": "MESSAGING_DELIVER_REQUEST"
}
```

Client success response

```json
{
  "payload": {
    "message_id": "<int>"
  },
  "type": "MESSAGING_DELIVER_SUCCESS"
}
```

Client failure response

```json
{
  "payload": {
    "errors": ["<string>"]
  },
  "type": "MESSAGING_DELIVER_FAILURE"
}
```

### Connection

Client request

```json
{
  "payload": {
  },
  "type": "CONN_KEEP_ALIVE_REQUEST"
}
```

Server success response

```json
{
  "payload": {
  },
  "type": "CONN_KEEP_ALIVE_SUCCESS"
}
```

Server failure response

```json
{
  "payload": {
  },
  "type": "CONN_KEEP_ALIVE_FAILURE"
}
```
