> [!IMPORTANT]
> Current API version is v9.
>
> This guide is primarily for Discord **ACCOUNT** tokens, not **BOT** tokens.

# Table of Contents
- [Headers](#headers)
  - [User-Agent](#user-agent)
  - [X-Super-Properties (Xsup)](#x-super-properties-xsup)
  - [X-Super-Properties (Xsup) Decoded](#x-super-properties-xsup-decoded)
  - [Authorization](#authorization)
  - [Cookies](#cookies)
  - [Best Universal Headers](#best-universal-headers)
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

# Headers

## User-Agent
> Note: Different browsers have different user agents. Using an outdated or unknown user agent may result in detection.

```json
{
    "User-Agent": ""
}
```

## X-Super-Properties (Xsup)
> Note: Xsup can be decoded using base64. They should be updated after every Discord update.

```json
{
    "X-Super-Properties": ""
}
```

## X-Super-Properties (Xsup) Decoded
> Note: These values are from the Discord app as of 30/07/2024.

```json
{
    "os": "Windows",
    "browser": "Discord Client",
    "release_channel": "stable",
    "client_version": "1.0.9155",
    "os_version": "10.0.22631",
    "os_arch": "x64",
    "app_arch": "x64",
    "system_locale": "en-GB",
    "browser_user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) discord/1.0.9155 Chrome/124.0.6367.243 Electron/30.2.0 Safari/537.36",
    "browser_version": "30.2.0",
    "client_build_number": 313344,
    "native_build_number": 49817,
    "client_event_source": null
}
```

## Authorization
> Note: A Discord **ACCOUNT** token should be inputted here.

```json
{
    "Authorization": ""
}
```

## Cookies
> Note: The value needs to be correctly formatted. Static cookies will be detected over time.

```json
{
    "Cookie": ""
}
```

## Best Universal Headers
> Note: Replace all placeholder values.

```python
headers = {
    'Accept': '*/*',
    'Accept-Encoding': 'gzip, deflate, br',
    'Accept-Language': 'en-GB,pl;q=0.9',
    'Authorization': '',  # Replace with account token
    'Cookie': '',  # Replace with correctly formatted cookies
    'Content-Type': 'application/json',
    'Origin': 'https://discord.com',
    'Priority': 'u=1, i',
    'Sec-Ch-Ua': '"Not-A.Brand";v="99", "Chromium";v="124"',
    'Sec-Ch-Ua-Mobile': '?0',
    'Sec-Ch-Ua-Platform': '"Windows"',
    'Sec-Fetch-Dest': 'empty',
    'Sec-Fetch-Mode': 'cors',
    'Sec-Fetch-Site': 'same-origin',
    'User-Agent': '',  # Replace with user agent
    'X-Debug-Options': 'bugReporterEnabled',
    'X-Discord-Locale': 'en-US',
    'X-Discord-Timezone': 'Europe/Berlin',
    'X-Super-Properties': ''  # Replace with xsup
}
```

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

# Open a DM

```
Endpoint: https://discord.com/api/v9/users/@me/channels
Method: POST
Status Code: 200
Payload:
{
    'recipients': [userid]
}
```
