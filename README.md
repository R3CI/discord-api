# Discord API v9 Endpoints

> [!IMPORTANT]
> Last update 02.07.2025
> 
> Current API version is v9
>
> If this helped you make sure to star ⭐
>
> This guide will NOT tell you about api restrictions and how to go about them (and cant post that cause of github) if you want a guide and info check out my shop 

Did not find what you are looking for? Check this https://discord.com/developers/docs/reference

# Table of Contents
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
- [Open a DM](#open-a-dm)
- [Get User Info](#get-user-info)
- [Get Server Info](#get-server-info)
- [Get Channel Info](#get-channel-info)
- [Create Channel](#create-channel)
- [Delete Channel](#delete-channel)
- [Modify Channel](#modify-channel)
- [Get Server Members](#get-server-members)
- [Kick Member](#kick-member)
- [Ban Member](#ban-member)
- [Unban Member](#unban-member)
- [Modify Member](#modify-member)
- [Add Role to Member](#add-role-to-member)
- [Remove Role from Member](#remove-role-from-member)
- [Create Role](#create-role)
- [Modify Role](#modify-role)
- [Delete Role](#delete-role)
- [Create Invite](#create-invite)
- [Get Invites](#get-invites)
- [Delete Invite](#delete-invite)
- [Pin Message](#pin-message)
- [Unpin Message](#unpin-message)
- [Get Pinned Messages](#get-pinned-messages)
- [Start Typing](#start-typing)
- [Get Voice Regions](#get-voice-regions)
- [Modify Server](#modify-server)
- [Create Emoji](#create-emoji)
- [Modify Emoji](#modify-emoji)
- [Delete Emoji](#delete-emoji)
- [Create Webhook](#create-webhook)
- [Get Webhooks](#get-webhooks)
- [Modify Webhook](#modify-webhook)
- [Delete Webhook](#delete-webhook)
- [Execute Webhook](#execute-webhook)
- [Authorize OAuth2 App](#authorize-oauth2-app)
- [Get Current User](#get-current-user)
- [Modify Current User](#modify-current-user)
- [Get Current User Guilds](#get-current-user-guilds)
- [Create Group DM](#create-group-dm)
- [Add Recipient to Group DM](#add-recipient-to-group-dm)
- [Remove Recipient from Group DM](#remove-recipient-from-group-dm)
- [Create Thread](#create-thread)
- [Join Thread](#join-thread)
- [Leave Thread](#leave-thread)
- [Add Thread Member](#add-thread-member)
- [Remove Thread Member](#remove-thread-member)
- [Get Thread Member](#get-thread-member)
- [List Thread Members](#list-thread-members)
- [Get Active Threads](#get-active-threads)
- [Get Public Archived Threads](#get-public-archived-threads)
- [Get Private Archived Threads](#get-private-archived-threads)
- [Get Joined Private Archived Threads](#get-joined-private-archived-threads)
- [Create Slash Command](#create-slash-command)
- [Get Slash Commands](#get-slash-commands)
- [Edit Slash Command](#edit-slash-command)
- [Delete Slash Command](#delete-slash-command)
- [Bulk Overwrite Slash Commands](#bulk-overwrite-slash-commands)
- [Create Interaction Response](#create-interaction-response)
- [Edit Original Interaction Response](#edit-original-interaction-response)
- [Delete Original Interaction Response](#delete-original-interaction-response)
- [Create Followup Message](#create-followup-message)
- [Edit Followup Message](#edit-followup-message)
- [Delete Followup Message](#delete-followup-message)
- [Get Application](#get-application)
- [Edit Application](#edit-application)
- [Create Stage Instance](#create-stage-instance)
- [Get Stage Instance](#get-stage-instance)
- [Modify Stage Instance](#modify-stage-instance)
- [Delete Stage Instance](#delete-stage-instance)
- [Get Sticker](#get-sticker)
- [List Nitro Sticker Packs](#list-nitro-sticker-packs)
- [List Guild Stickers](#list-guild-stickers)
- [Get Guild Sticker](#get-guild-sticker)
- [Create Guild Sticker](#create-guild-sticker)
- [Modify Guild Sticker](#modify-guild-sticker)
- [Delete Guild Sticker](#delete-guild-sticker)
- [Get Gateway](#get-gateway)
- [Get Gateway Bot](#get-gateway-bot)
- [Get User Connections](#get-user-connections)
- [Get Guild Template](#get-guild-template)
- [Create Guild from Template](#create-guild-from-template)
- [Get Guild Templates](#get-guild-templates)
- [Create Guild Template](#create-guild-template)
- [Sync Guild Template](#sync-guild-template)
- [Modify Guild Template](#modify-guild-template)
- [Delete Guild Template](#delete-guild-template)
- [Modify Guild Welcome Screen](#modify-guild-welcome-screen)
- [Get Guild Welcome Screen](#get-guild-welcome-screen)
- [Modify Current User Voice State](#modify-current-user-voice-state)
- [Modify User Voice State](#modify-user-voice-state)
- [Follow News Channel](#follow-news-channel)
- [Crosspost Message](#crosspost-message)
- [Get Guild Audit Log](#get-guild-audit-log)
- [Get Guild Bans](#get-guild-bans)
- [Get Guild Ban](#get-guild-ban)
- [Get Guild Prune Count](#get-guild-prune-count)
- [Begin Guild Prune](#begin-guild-prune)
- [Get Guild Voice Regions](#get-guild-voice-regions)
- [Get Guild Integrations](#get-guild-integrations)
- [Delete Guild Integration](#delete-guild-integration)
- [Get Guild Widget Settings](#get-guild-widget-settings)
- [Modify Guild Widget](#modify-guild-widget)
- [Get Guild Widget](#get-guild-widget)
- [Get Guild Vanity URL](#get-guild-vanity-url)
- [Get Guild Widget Image](#get-guild-widget-image)
- [Search Guild Members](#search-guild-members)
- [Get Reactions](#get-reactions)
- [Delete All Reactions](#delete-all-reactions)
- [Delete All Reactions for Emoji](#delete-all-reactions-for-emoji)
- [Bulk Delete Messages](#bulk-delete-messages)
- [Edit Channel Permissions](#edit-channel-permissions)
- [Delete Channel Permission](#delete-channel-permission)
- [Trigger Typing Indicator](#trigger-typing-indicator)
- [Get Channel Webhooks](#get-channel-webhooks)
- [Get Guild Webhooks](#get-guild-webhooks)
- [Get Webhook](#get-webhook)
- [Get Webhook with Token](#get-webhook-with-token)
- [Modify Webhook with Token](#modify-webhook-with-token)
- [Delete Webhook with Token](#delete-webhook-with-token)
- [Execute Slack Compatible Webhook](#execute-slack-compatible-webhook)
- [Execute GitHub Compatible Webhook](#execute-github-compatible-webhook)
- [Get Webhook Message](#get-webhook-message)
- [Edit Webhook Message](#edit-webhook-message)
- [Delete Webhook Message](#delete-webhook-message)
- [Report Message](#report-message)
- [Get Application Role Connection Metadata](#get-application-role-connection-metadata)
- [Update Application Role Connection Metadata](#update-application-role-connection-metadata)
- [Get User Application Role Connection](#get-user-application-role-connection)
- [Update User Application Role Connection](#update-user-application-role-connection)
- [Create Auto Moderation Rule](#create-auto-moderation-rule)
- [Get Auto Moderation Rules](#get-auto-moderation-rules)
- [Get Auto Moderation Rule](#get-auto-moderation-rule)
- [Modify Auto Moderation Rule](#modify-auto-moderation-rule)
- [Delete Auto Moderation Rule](#delete-auto-moderation-rule)
- [List Scheduled Events](#list-scheduled-events)
- [Create Scheduled Event](#create-scheduled-event)
- [Get Scheduled Event](#get-scheduled-event)
- [Modify Scheduled Event](#modify-scheduled-event)
- [Delete Scheduled Event](#delete-scheduled-event)
- [Get Scheduled Event Users](#get-scheduled-event-users)

## Join
```
URL https://discord.com/api/v9/invites/{inviteregex}
Method POST
Succeded status 200
Payload
{
    'session_id': {sessionid}
}
```

## Leave
```
URL https://discord.com/api/v9/users/@me/guilds/{serverid}
Method DELETE
Succeded status 204
```

## Check If in Server
```
URL https://discord.com/api/v9/guilds/{serverid}
Method GET
Succeded status 200
Payload
{
    'lurking': False
}
```

## Send a Message
```
URL https://discord.com/api/v9/channels/{channelid}/messages
Method POST
Succeded status 200
Payload
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
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}
Method DELETE
Succeded status 204
```

## Edit a Message
```
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}
Method PATCH
Succeded status 200
Payload: 
{
    'content': {newmessage}
}
```

## Get Messages
```
URL https://discord.com/api/v9/channels/{channelid}/messages?limit=50
Method GET
Succeded status 200
```

## React to a message
```
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/reactions/{emoji}/@me
Method PUT
Succeded status 204
```

## Dereact from a message
```
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/reactions/{emoji}/@me
Method DELETE
Succeded status 204
```

## Click a button
```
URL https://discord.com/api/v9/interactions
Method POST
Succeded status 204
Payload
{
    'type': 3,
    'nonce': {nonce},
    'guild_id': {serverid},
    'channel_id': {channelid},
    'message_flags': 0,
    'message_id': {messageid},
    'application_id': {applicationid},
    'session_id': {sessionid},
    'data': {
        'component_type': 2,
        'custom_id': {customid}
    }
}
```

## Authorize OAuth2 App
```
URL https://discord.com/api/v9/oauth2/authorize
Method POST
Succeded status 302
```

## Get Current User
```
URL https://discord.com/api/v9/users/@me
Method GET
Succeded status 200
```

## Modify Current User
```
URL https://discord.com/api/v9/users/@me
Method PATCH
Succeded status 200
```

## Get Current User Guilds
```
URL https://discord.com/api/v9/users/@me/guilds
Method GET
Succeded status 200
```

## Create Group DM
```
URL https://discord.com/api/v9/users/@me/channels
Method POST
Succeded status 200
```

## Add Recipient to Group DM
```
URL https://discord.com/api/v9/channels/{channelid}/recipients/{userid}
Method PUT
Succeded status 204
```

## Remove Recipient from Group DM
```
URL https://discord.com/api/v9/channels/{channelid}/recipients/{userid}
Method DELETE
Succeded status 204
```

## Create Thread
```
URL https://discord.com/api/v9/channels/{channelid}/threads
Method POST
Succeded status 201
```

## Join Thread
```
URL https://discord.com/api/v9/channels/{channelid}/thread-members/@me
Method PUT
Succeded status 204
```

## Leave Thread
```
URL https://discord.com/api/v9/channels/{channelid}/thread-members/@me
Method DELETE
Succeded status 204
```

## Add Thread Member
```
URL https://discord.com/api/v9/channels/{channelid}/thread-members/{userid}
Method PUT
Succeded status 204
```

## Remove Thread Member
```
URL https://discord.com/api/v9/channels/{channelid}/thread-members/{userid}
Method DELETE
Succeded status 204
```

## Get Thread Member
```
URL https://discord.com/api/v9/channels/{channelid}/thread-members/{userid}
Method GET
Succeded status 200
```

## List Thread Members
```
URL https://discord.com/api/v9/channels/{channelid}/thread-members
Method GET
Succeded status 200
```

## Get Active Threads
```
URL https://discord.com/api/v9/channels/{channelid}/threads/active
Method GET
Succeded status 200
```

## Get Public Archived Threads
```
URL https://discord.com/api/v9/channels/{channelid}/threads/archived/public
Method GET
Succeded status 200
```

## Get Private Archived Threads
```
URL https://discord.com/api/v9/channels/{channelid}/threads/archived/private
Method GET
Succeded status 200
```

## Get Joined Private Archived Threads
```
URL https://discord.com/api/v9/channels/{channelid}/users/@me/threads/archived/private
Method GET
Succeded status 200
```

## Create Slash Command
```
URL https://discord.com/api/v9/applications/{applicationid}/commands
Method POST
Succeded status 201
```

## Get Slash Commands
```
URL https://discord.com/api/v9/applications/{applicationid}/commands
Method GET
Succeded status 200
```

## Edit Slash Command
```
URL https://discord.com/api/v9/applications/{applicationid}/commands/{commandid}
Method PATCH
Succeded status 200
```

## Delete Slash Command
```
URL https://discord.com/api/v9/applications/{applicationid}/commands/{commandid}
Method DELETE
Succeded status 204
```

## Bulk Overwrite Slash Commands
```
URL https://discord.com/api/v9/applications/{applicationid}/commands
Method PUT
Succeded status 200
```

## Create Interaction Response
```
URL https://discord.com/api/v9/interactions/{interactionid}/{interactiontoken}/callback
Method POST
Succeded status 204
```

## Edit Original Interaction Response
```
URL https://discord.com/api/v9/webhooks/{applicationid}/{interactiontoken}/messages/@original
Method PATCH
Succeded status 200
```

## Delete Original Interaction Response
```
URL https://discord.com/api/v9/webhooks/{applicationid}/{interactiontoken}/messages/@original
Method DELETE
Succeded status 204
```

## Create Followup Message
```
URL https://discord.com/api/v9/webhooks/{applicationid}/{interactiontoken}
Method POST
Succeded status 200
```

## Edit Followup Message
```
URL https://discord.com/api/v9/webhooks/{applicationid}/{interactiontoken}/messages/{messageid}
Method PATCH
Succeded status 200
```

## Delete Followup Message
```
URL https://discord.com/api/v9/webhooks/{applicationid}/{interactiontoken}/messages/{messageid}
Method DELETE
Succeded status 204
```

## Get Application
```
URL https://discord.com/api/v9/applications/@me
Method GET
Succeded status 200
```

## Edit Application
```
URL https://discord.com/api/v9/applications/@me
Method PATCH
Succeded status 200
```

## Create Stage Instance
```
URL https://discord.com/api/v9/stage-instances
Method POST
Succeded status 200
```

## Get Stage Instance
```
URL https://discord.com/api/v9/stage-instances/{channelid}
Method GET
Succeded status 200
```

## Modify Stage Instance
```
URL https://discord.com/api/v9/stage-instances/{channelid}
Method PATCH
Succeded status 200
```

## Delete Stage Instance
```
URL https://discord.com/api/v9/stage-instances/{channelid}
Method DELETE
Succeded status 204
```

## Get Sticker
```
URL https://discord.com/api/v9/stickers/{stickerid}
Method GET
Succeded status 200
```

## List Nitro Sticker Packs
```
URL https://discord.com/api/v9/sticker-packs
Method GET
Succeded status 200
```

## List Guild Stickers
```
URL https://discord.com/api/v9/guilds/{guildid}/stickers
Method GET
Succeded status 200
```

## Get Guild Sticker
```
URL https://discord.com/api/v9/guilds/{guildid}/stickers/{stickerid}
Method GET
Succeded status 200
```

## Create Guild Sticker
```
URL https://discord.com/api/v9/guilds/{guildid}/stickers
Method POST
Succeded status 201
```

## Modify Guild Sticker
```
URL https://discord.com/api/v9/guilds/{guildid}/stickers/{stickerid}
Method PATCH
Succeded status 200
```

## Delete Guild Sticker
```
URL https://discord.com/api/v9/guilds/{guildid}/stickers/{stickerid}
Method DELETE
Succeded status 204
```

## Get Gateway
```
URL https://discord.com/api/v9/gateway
Method GET
Succeded status 200
```

## Get Gateway Bot
```
URL https://discord.com/api/v9/gateway/bot
Method GET
Succeded status 200
```

## Get User Connections
```
URL https://discord.com/api/v9/users/@me/connections
Method GET
Succeded status 200
```

## Get Guild Template
```
URL https://discord.com/api/v9/guilds/templates/{templatecode}
Method GET
Succeded status 200
```

## Create Guild from Template
```
URL https://discord.com/api/v9/guilds/templates/{templatecode}
Method POST
Succeded status 201
```

## Get Guild Templates
```
URL https://discord.com/api/v9/guilds/{guildid}/templates
Method GET
Succeded status 200
```

## Create Guild Template
```
URL https://discord.com/api/v9/guilds/{guildid}/templates
Method POST
Succeded status 200
```

## Sync Guild Template
```
URL https://discord.com/api/v9/guilds/{guildid}/templates/{templatecode}
Method PUT
Succeded status 200
```

## Modify Guild Template
```
URL https://discord.com/api/v9/guilds/{guildid}/templates/{templatecode}
Method PATCH
Succeded status 200
```

## Delete Guild Template
```
URL https://discord.com/api/v9/guilds/{guildid}/templates/{templatecode}
Method DELETE
Succeded status 200
```

## Modify Guild Welcome Screen
```
URL https://discord.com/api/v9/guilds/{guildid}/welcome-screen
Method PATCH
Succeded status 200
```

## Get Guild Welcome Screen
```
URL https://discord.com/api/v9/guilds/{guildid}/welcome-screen
Method GET
Succeded status 200
```

## Modify Current User Voice State
```
URL https://discord.com/api/v9/guilds/{guildid}/voice-states/@me
Method PATCH
Succeded status 204
```

## Modify User Voice State
```
URL https://discord.com/api/v9/guilds/{guildid}/voice-states/{userid}
Method PATCH
Succeded status 204
```

## Follow News Channel
```
URL https://discord.com/api/v9/channels/{channelid}/followers
Method POST
Succeded status 200
```

## Crosspost Message
```
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/crosspost
Method POST
Succeded status 200
```

## Get Guild Audit Log
```
URL https://discord.com/api/v9/guilds/{guildid}/audit-logs
Method GET
Succeded status 200
```

## Get Guild Bans
```
URL https://discord.com/api/v9/guilds/{guildid}/bans
Method GET
Succeded status 200
```

## Get Guild Ban
```
URL https://discord.com/api/v9/guilds/{guildid}/bans/{userid}
Method GET
Succeded status 200
```

## Get Guild Prune Count
```
URL https://discord.com/api/v9/guilds/{guildid}/prune
Method GET
Succeded status 200
```

## Begin Guild Prune
```
URL https://discord.com/api/v9/guilds/{guildid}/prune
Method POST
Succeded status 200
```

## Get Guild Voice Regions
```
URL https://discord.com/api/v9/guilds/{guildid}/regions
Method GET
Succeded status 200
```

## Get Guild Integrations
```
URL https://discord.com/api/v9/guilds/{guildid}/integrations
Method GET
Succeded status 200
```

## Delete Guild Integration
```
URL https://discord.com/api/v9/guilds/{guildid}/integrations/{integrationid}
Method DELETE
Succeded status 204
```

## Get Guild Widget Settings
```
URL https://discord.com/api/v9/guilds/{guildid}/widget
Method GET
Succeded status 200
```

## Modify Guild Widget
```
URL https://discord.com/api/v9/guilds/{guildid}/widget
Method PATCH
Succeded status 200
```

## Get Guild Widget
```
URL https://discord.com/api/v9/guilds/{guildid}/widget.json
Method GET
Succeded status 200
```

## Get Guild Vanity URL
```
URL https://discord.com/api/v9/guilds/{guildid}/vanity-url
Method GET
Succeded status 200
```

## Get Guild Widget Image
```
URL https://discord.com/api/v9/guilds/{guildid}/widget.png
Method GET
Succeded status 200
```

## Search Guild Members
```
URL https://discord.com/api/v9/guilds/{guildid}/members/search
Method GET
Succeded status 200
```

## Get Reactions
```
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/reactions/{emoji}
Method GET
Succeded status 200
```

## Delete All Reactions
```
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/reactions
Method DELETE
Succeded status 204
```

## Delete All Reactions for Emoji
```
URL https://discord.com/api/v9/channels/{channelid}/messages/{messageid}/reactions/{emoji}
Method DELETE
Succeded status 204
```

## Bulk Delete Messages
```
URL https://discord.com/api/v9/channels/{channelid}/messages/bulk-delete
Method POST
Succeded status 204
```

## Edit Channel Permissions
```
URL https://discord.com/api/v9/channels/{channelid}/permissions/{overwriteid}
Method PUT
Succeded status 204
```

## Delete Channel Permission
```
URL https://discord.com/api/v9/channels/{channelid}/permissions/{overwriteid}
Method DELETE
Succeded status 204
```

## Trigger Typing Indicator
```
URL https://discord.com/api/v9/channels/{channelid}/typing
Method POST
Succeded status 204
```

## Get Channel Webhooks
```
URL https://discord.com/api/v9/channels/{channelid}/webhooks
Method GET
Succeded status 200
```

## Get Guild Webhooks
```
URL https://discord.com/api/v9/guilds/{guildid}/webhooks
Method GET
Succeded status 200
```

## Get Webhook
```
URL https://discord.com/api/v9/webhooks/{webhookid}
Method GET
Succeded status 200
```

## Get Webhook with Token
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}
Method GET
Succeded status 200
```

## Modify Webhook with Token
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}
Method PATCH
Succeded status 200
```

## Delete Webhook with Token
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}
Method DELETE
Succeded status 204
```

## Execute Slack Compatible Webhook
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}/slack
Method POST
Succeded status 204
```

## Execute GitHub Compatible Webhook
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}/github
Method POST
Succeded status 204
```

## Get Webhook Message
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}/messages/{messageid}
Method GET
Succeded status 200
```

## Edit Webhook Message
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}/messages/{messageid}
Method PATCH
Succeded status 200
```

## Delete Webhook Message
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}/messages/{messageid}
Method DELETE
Succeded status 204
```

## Report Message
```
URL https://discord.com/api/v9/reporting/message
Method POST
Succeded status 201
```

## Get Application Role Connection Metadata
```
URL https://discord.com/api/v9/applications/{applicationid}/role-connections/metadata
Method GET
Succeded status 200
```

## Update Application Role Connection Metadata
```
URL https://discord.com/api/v9/applications/{applicationid}/role-connections/metadata
Method PUT
Succeded status 200
```

## Get User Application Role Connection
```
URL https://discord.com/api/v9/users/@me/applications/{applicationid}/role-connection
Method GET
Succeded status 200
```

## Update User Application Role Connection
```
URL https://discord.com/api/v9/users/@me/applications/{applicationid}/role-connection
Method PUT
Succeded status 200
```

## Create Auto Moderation Rule
```
URL https://discord.com/api/v9/guilds/{guildid}/auto-moderation/rules
Method POST
Succeded status 200
```

## Get Auto Moderation Rules
```
URL https://discord.com/api/v9/guilds/{guildid}/auto-moderation/rules
Method GET
Succeded status 200
```

## Get Auto Moderation Rule
```
URL https://discord.com/api/v9/guilds/{guildid}/auto-moderation/rules/{ruleid}
Method GET
Succeded status 200
```

## Modify Auto Moderation Rule
```
URL https://discord.com/api/v9/guilds/{guildid}/auto-moderation/rules/{ruleid}
Method PATCH
Succeded status 200
```

## Delete Auto Moderation Rule
```
URL https://discord.com/api/v9/guilds/{guildid}/auto-moderation/rules/{ruleid}
Method DELETE
Succeded status 204
```

## List Scheduled Events
```
URL https://discord.com/api/v9/guilds/{guildid}/scheduled-events
Method GET
Succeded status 200
```

## Create Scheduled Event
```
URL https://discord.com/api/v9/guilds/{guildid}/scheduled-events
Method POST
Succeded status 200
```

## Get Scheduled Event
```
URL https://discord.com/api/v9/guilds/{guildid}/scheduled-events/{evenid}
Method GET
Succeded status 200
```

## Modify Scheduled Event
```
URL https://discord.com/api/v9/guilds/{guildid}/scheduled-events/{eventid}
Method PATCH
Succeded status 200
```

## Delete Scheduled Event
```
URL https://discord.com/api/v9/guilds/{guildid}/scheduled-events/{eventid}
Method DELETE
Succeded status 204
```

## Get Scheduled Event Users
```
URL https://discord.com/api/v9/guilds/{guildid}/scheduled-events/{eventid}/users
Method GET
Succeded status 200
```

## Open a DM
```
URL https://discord.com/api/v9/users/@me/channels
Method POST
Succeded status 200
Payload
{
    'recipients': [userid]
}
```

## Get User Info
```
URL https://discord.com/api/v9/users/{userid}
Method GET
Succeded status 200
```

## Get Server Info
```
URL https://discord.com/api/v9/guilds/{serverid}
Method GET
Succeded status 200
```

## Get Channel Info
```
URL https://discord.com/api/v9/channels/{channelid}
Method GET
Succeded status 200
```

## Create Channel
```
URL https://discord.com/api/v9/guilds/{serverid}/channels
Method POST
Succeded status 201
Payload
{
    'name': {channelname},
    'type': {channeltype},  # 0 = text, 2 = voice, 4 = category
    'topic': {topic},
    'parent_id': {categoryid}
}
```

## Delete Channel
```
URL https://discord.com/api/v9/channels/{channelid}
Method DELETE
Succeded status 200
```

## Modify Channel
```
URL https://discord.com/api/v9/channels/{channelid}
Method PATCH
Succeded status 200
Payload
{
    'name': {newname},
    'topic': {newtopic},
    'position': {position}
}
```

## Get Server Members
```
URL https://discord.com/api/v9/guilds/{serverid}/members?limit=1000
Method GET
Succeded status 200
```

## Kick Member
```
URL https://discord.com/api/v9/guilds/{serverid}/members/{userid}
Method DELETE
Succeded status 204
```

## Ban Member
```
URL https://discord.com/api/v9/guilds/{serverid}/bans/{userid}
Method PUT
Succeded status 204
Payload
{
    'delete_message_days': {days},  # 0-7 days
    'reason': {reason}
}
```

## Unban Member
```
URL https://discord.com/api/v9/guilds/{serverid}/bans/{userid}
Method DELETE
Succeded status 204
```

## Modify Member
```
URL https://discord.com/api/v9/guilds/{serverid}/members/{userid}
Method PATCH
Succeded status 200
Payload
{
    'nick': {newnickname},
    'roles': [{roleid1}, {roleid2}],
    'mute': {boolean},
    'deaf': {boolean}
}
```

## Add Role to Member
```
URL https://discord.com/api/v9/guilds/{serverid}/members/{userid}/roles/{roleid}
Method PUT
Succeded status 204
```

## Remove Role from Member
```
URL https://discord.com/api/v9/guilds/{serverid}/members/{userid}/roles/{roleid}
Method DELETE
Succeded status 204
```

## Create Role
```
URL https://discord.com/api/v9/guilds/{serverid}/roles
Method POST
Succeded status 200
Payload
{
    'name': {rolename},
    'permissions': {permissions},  # bitwise permissions
    'color': {color},  # decimal color
    'hoist': {boolean},  # display separately
    'mentionable': {boolean}
}
```

## Modify Role
```
URL https://discord.com/api/v9/guilds/{serverid}/roles/{roleid}
Method PATCH
Succeded status 200
Payload
{
    'name': {newname},
    'permissions': {newpermissions},
    'color': {newcolor},
    'hoist': {boolean},
    'mentionable': {boolean}
}
```

## Delete Role
```
URL https://discord.com/api/v9/guilds/{serverid}/roles/{roleid}
Method DELETE
Succeded status 204
```

## Create Invite
```
URL https://discord.com/api/v9/channels/{channelid}/invites
Method POST
Succeded status 200
Payload
{
    'max_age': {seconds},  # 0 = never expire
    'max_uses': {uses},  # 0 = unlimited
    'temporary': {boolean},
    'unique': {boolean}
}
```

## Get Invites
```
URL https://discord.com/api/v9/guilds/{serverid}/invites
Method GET
Succeded status 200
```

## Delete Invite
```
URL https://discord.com/api/v9/invites/{invitecode}
Method DELETE
Succeded status 200
```

## Pin Message
```
URL https://discord.com/api/v9/channels/{channelid}/pins/{messageid}
Method PUT
Succeded status 204
```

## Unpin Message
```
URL https://discord.com/api/v9/channels/{channelid}/pins/{messageid}
Method DELETE
Succeded status 204
```

## Get Pinned Messages
```
URL https://discord.com/api/v9/channels/{channelid}/pins
Method GET
Succeded status 200
```

## Start Typing
```
URL https://discord.com/api/v9/channels/{channelid}/typing
Method POST
Succeded status 204
```

## Get Voice Regions
```
URL https://discord.com/api/v9/voice/regions
Method GET
Succeded status 200
```

## Modify Server
```
URL https://discord.com/api/v9/guilds/{serverid}
Method PATCH
Succeded status 200
Payload
{
    'name': {newname},
    'region': {region},
    'verification_level': {level},  # 0-4
    'default_message_notifications': {level},  # 0-1
    'explicit_content_filter': {level}  # 0-2
}
```

## Create Emoji
```
URL https://discord.com/api/v9/guilds/{serverid}/emojis
Method POST
Succeded status 201
Payload
{
    'name': {emojiname},
    'image': {base64image},
    'roles': [{roleid1}, {roleid2}]
}
```

## Modify Emoji
```
URL https://discord.com/api/v9/guilds/{serverid}/emojis/{emojiid}
Method PATCH
Succeded status 200
Payload
{
    'name': {newname},
    'roles': [{roleid1}, {roleid2}]
}
```

## Delete Emoji
```
URL https://discord.com/api/v9/guilds/{serverid}/emojis/{emojiid}
Method DELETE
Succeded status 204
```

## Create Webhook
```
URL https://discord.com/api/v9/channels/{channelid}/webhooks
Method POST
Succeded status 200
Payload
{
    'name': {webhookname},
    'avatar': {base64avatar}
}
```

## Get Webhooks
```
URL https://discord.com/api/v9/channels/{channelid}/webhooks
Method GET
Succeded status 200
```

## Modify Webhook
```
URL https://discord.com/api/v9/webhooks/{webhookid}
Method PATCH
Succeded status 200
Payload
{
    'name': {newname},
    'avatar': {newavatar},
    'channel_id': {newchannelid}
}
```

## Delete Webhook
```
URL https://discord.com/api/v9/webhooks/{webhookid}
Method DELETE
Succeded status 204
```

## Execute Webhook
```
URL https://discord.com/api/v9/webhooks/{webhookid}/{webhooktoken}
Method POST
Succeded status 204
Payload
{
    'content': {message},
    'username': {overrideusername},
    'avatar_url': {overrideavatar},
    'tts': {boolean},
    'embeds': [{embedobject}]
}
```
