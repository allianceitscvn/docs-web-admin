# Web Push

## Prepare

* Frontend has service\_worker.js
* Server web push
* Pair key: PUBLIC\_VAPID\_KEY/PRIVATE\_VAPID\_KEY

## Generator VAPID KEY

* Generate key from firebase
* Using website online [https://vapidkeys.com/](https://vapidkeys.com/)
* Run command:

```
./node_modules/.bin/web-push generate-vapid-keys
```

Example result:

```json
{
    "subject": "mailto: <zgknrwnzabi@knowledgemd.com>",
    "publicKey": "BOtkk7H3bMg1nDGhU2bLXV-vyOX3WlyGj7gXlzooGyNjrrJfYJa8OxnkL_8GHWQVTzyfbXQWVuGQL-AzZlHPs_8",
    "privateKey": "sCQvuhyEnMSmjhWTg3_UIosbTxCUqYqQnZEHwVB1krk"
}
```
