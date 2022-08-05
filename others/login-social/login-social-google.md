# Login Social: Google

## Setup Google Client ID

Go to site credential of console google

![](<../../.gitbook/assets/image (4).png>)

Configure your consent screen

Check Authorized JavaScript origins and Authorized redirect URIs

Get Client Id to config in website

![](<../../.gitbook/assets/image (2).png>)

## Config in config website

Enable login google and setup google client ID in \_config.js

```json
{
    "hasLoginSocialGoogle":true,
    "GoogleClientId": "GoogleClientId",
}
```
