> [!IMPORTANT]
> Current api version is v9
>
> This is made mainly for discord **ACCOUNT** tokens not **BOT** tokens


# Table of contents
- [Headers](#headers)


# Headers
Most impotant headers:
- User-Agent
- X-Super-Properties
- Authorization
- Cookies

### User-Agent
Note: Most browsers will have a diffrent user agent, if you use a outdated or unknown user agent you will get detected

```json
{
    "User-Agent": ""
}
```

### X-Super-Propetries (Xsup)
Note: Xsup can be decoed using base64, they should be updated after every discord update

```json
{
    "X-Super-Properties": ""
}
```

### X-Super-Propetries (Xsup) decoed
Note: They are from the discord app taken at 30/7/2024

```json
{
    "os":"Windows",
    "browser":"Discord Client",
    "release_channel":"stable",
    "client_version":"1.0.9155",
    "os_version":"10.0.22631",
    "os_arch":"x64",
    "app_arch":"x64",
    "system_locale":"en-GB",
    "browser_user_agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) discord/1.0.9155 Chrome/124.0.6367.243 Electron/30.2.0 Safari/537.36",
    "browser_version":"30.2.0",
    "client_build_number":313344,
    "native_build_number":49817,
    "client_event_source":null
}
```

### Authentication
Note: A discord **ACCOUNT** token should be inputted in here

```json
{
    "Authentication": ""
}
```

### Cookies
Note: The value needs to be correctly formatted, static cookies will get detected over time

```json
{
    "Cookie": ""
}
```

### Best universal headers
Note: Replace all the values that have a comment next to them

```python
headers = {
    'Accept': '*/*',
    'Accept-Encoding': 'gzip, deflate, br',
    'Accept-Language': 'en-GB,pl;q=0.9',
    'Authorization': '', # replace with a account token
    'Cookie': '', # replace with cookies (Need to be correctly formatted)
    'Content-Type': 'application/json',
    'Origin': 'https://discord.com',
    'Priority': 'u=1, i',
    'Sec-Ch-Ua': '"Not-A.Brand";v="99", "Chromium";v="124"',
    'Sec-Ch-Ua-Mobile': '?0',
    'Sec-Ch-Ua-Platform': '"Windows"',
    'Sec-Fetch-Dest': 'empty',
    'Sec-Fetch-Mode': 'cors',
    'Sec-Fetch-Site': 'same-origin',
    'User-Agent': '', # replace with the user agent
    'X-Debug-Options': 'bugReporterEnabled',
    'X-Discord-Locale': 'en-US',
    'X-Discord-Timezone': 'Europe/Berlin',
    'X-Super-Properties': '' # replace with xsup
}
```
