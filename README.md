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
