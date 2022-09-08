# Config Screen Page

Example config switch view

```json
  "Page": {
    "hasSwitchView": true,
    "listSwitchView": [
      "table",
      "list",
      "grid"
    ],
    "configCard": {
      "type": "with_myui",
      "myui": {
        "type": "data_obj",
        "style": {
          "background": "white",
          "borderRadius": "4px",
          "padding": "5px"
        },
        "configChild": {
          "type": "html",
          "moreProps": {
            "html": "Name: [Name]"
          }
        }
      }
    }
  }
```
