# Cell: with\_myui

### Example 1

#### Config

```json
"myui": {
  "type": "data_tag",
  "dataIsRow": true,
  "style": {
    "display": "flex",
    "alignItems": "center",
    "justifyContent": "center",
    "textAlign": "center"
  },
  "configChild": {
    "type": "data_tag",
    "tag": "span",
    "configChild": "[ApplicationStatusId_Name]",
    "style": {
      "background": "[ApplicationStatusId_Color]",
      "borderRadius": "10px",
      "padding": "0px 5px",
      "overflow": "hidden",
      "textOverflow": "ellipsis",
      "whiteSpace": "nowrap",
      "fontSize": "12px",
      "height": "20px"
    }
  }
}
```

#### Photo

![](<../../.gitbook/assets/image (5).png>)
