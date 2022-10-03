# Send Message Goggle Chat

## Các bước

1. Tạo Webhook URL từ Group Google Chat
   * Link có dạng: [https://chat.googleapis.com/v1/spaces/AAAAGCYeSRY/messages?key=AIza](https://chat.googleapis.com/v1/spaces/AAAAGCYeSRY/messages?key=AIza)...
2. Gọi URL web hook để send message
   * Gửi dạng POST
   * Có header là
     * ```
       'Content-Type': 'application/json; charset=UTF-8'
       ```
   * Có data là
     * ```
       'text': 'Hello from a Node script!'
       ```

## Nâng cao

#### Mention user

```
<users/USER_ID> <users/all>
```

#### Link

```
<https://example.com/foo|my link text>
```

Format

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## Tài liệu

{% embed url="https://developers.google.com/chat/how-tos/webhooks#node.js" %}

{% embed url="https://developers.google.com/chat/api/guides/message-formats/basic" %}
