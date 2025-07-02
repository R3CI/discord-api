> [!IMPORTANT]
> Last update 02.07.2025
> 
> Current API version is v9
>
> If this helped you make sure to star ⭐

Did not find what you are looking for? Check this https://discord.com/developers/docs/reference

# Table of Contents
- [Endpoints](#endpoints)
  - [Join](#join)
  - [Leave](#leave)
  - [Check If in Server](#check-if-in-server)
  - [Send a Message](#send-a-message)
  - [Delete a Message](#delete-a-message)
  - [Edit a Message](#edit-a-message)
  - [Get Messages](#get-messages)
  - [React to a message](#react-to-a-message)
  - [Dereact from a message](#dereact-from-a-message)
  - [Click a button](#click-a-button)
  - [Accept rules](#accept-rules)
  - [Bypass onboarding](#bypass-onboarding)
  - [Open a DM](#open-a-dm)

# Endpoints

## Join

```
Endpoint: https://discord.com/api/v9/invites/{regex}
Method: POST
Status Code: 200
```

## Leave

```
Endpoint: https://discord.com/api/v9/users/@me/guilds/{serverid}
Method: DELETE
Status Code: 204
Payload:
{
    'session_id': ''  # Replace with the session id (fake with uuid.uuid4().hex)
}
```

## Check If in Server

```
Endpoint: https://discord.com/api/v9/guilds/{serverid}
Method: GET
Status Code: 200 (means that it is inside)
Payload:
{
    'lurking': False
}
```

## Send a Message

```
Endpoint: https://discord.com/api/v9/channels/{channelid}/messages
Method: POST
Status Code: 200
Payload:
{
    'mobile_network_type': 'unknown',
    'content': {message},
    'nonce': {nonce},
    'tts': False,  # tts = text to speech
    'flags': 0
}
```

## Delete a Message

```
Endpoint: https://discord.com/api/v9/channels/{channelid}/messages/{messageid}
Method: DELETE
Status Code: 204
```

## Edit a Message

```
Endpoint: https://discord.com/api/v9/channels/{channelid}/messages/{messageid}
Method: PATCH
Status Code: 200
Payload: 
{
    'content': {newmessage}
}
```

## Get Messages

```
Endpoint: https://discord.com/api/v9/channels/{channelid}/messages?limit=50
Method: GET
Status Code: 200
```

## React to a Message

```
Endpoint: https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/reactions/{reaction}/%40me?location=Message&type=0
Method: PUT
Status Code: 204
```

## Dereact from a Message

```
Endpoint: https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/reactions/{reaction}/0/%40me?location=Message&burst=false
Method: DELETE
Status Code: 204
```

## Click a button

```
Endpoint: https://discord.com/api/v9/interactions
Method: POST
Status Code: 204
Payload:
}
    'application_id': authorid, # aka client id
    'channel_id': channelid,
    'data': {
        'component_type': 2,
        'custom_id': customid,
    },
    'guild_id': serverid,
    'message_flags': 0,
    'message_id': messageid,
    'nonce': nonce,
    'session_id': sessionid,
    'type': 3,
}
```

## Accept rules
> Note: The payload is annoying so be sure to test (FOR THIS PAYLAOD USE MY GET RULES!!!)

```
Endpoint: https://discord.com/api/v9/guilds/{serverid}/requests/@me
Method: PUT
Status Code: 201
Payload:
}
    'version': data['version'],
    'form_fields': [
        {
            'field_type': field['field_type'],
            'label': field['label'],
            'description': field['description'],
            'automations': field['automations'],
            'required': field['required'],
            'values': field['values'],
            'response': True
        } for field in data['form_fields']
    ]
}
```

## Bypass onboarding
> Note: Make sure you are using the correct instance for the payload values!!!

```
Endpoint: https://discord.com/api/v9/guilds/{serverid}/onboarding-responses
Method: PUT
Status Code: 200
Payload:
{
    'onboarding_responses': onboarding_responses, # LIST []
    'onboarding_prompts_seen': onboarding_prompts_seen, #  DICT {}
    'onboarding_responses_seen': onboarding_responses_seen# DICT {}
}
```

## Open a DM

```
Endpoint: https://discord.com/api/v9/users/@me/channels
Method: POST
Status Code: 200
Payload:
{
    'recipients': [userid]
}
```
