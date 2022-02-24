---
description: ConfigChart được trả về trong api Options
---

# Config Chart of Options

## Cấu trúc

```javascript
{
    "ChartConfig":{
        "Charts":[
            {
                "type":"type of MyChart",
                "fX":"",
                "fY":"",
                "titleX":"",
                "titleY":"",
                "titleChart":"",
                "options":"String JSON",
                "more":"String JSON"
            }
        ],
        "Config":{
            "DefaultShowContent": false,
            "configExpand": null,
            "styleWrapTabContent": null
        }
    }
}
```

## Config of ChartConfig

| Field Name          | Default Value |                                                         |
| ------------------- | ------------- | ------------------------------------------------------- |
| DefaultShowContent  | false         | Có mặc định show chart ra luôn hay để ẩn trong expander |
| configExpand        | null          | Config của vùng Expander Chart                          |
| styleWrapTabContent | null          | Style overide của vùng content                          |

### Cấu hình Config of ChartConfig ở ScreenConfig

![](<../.gitbook/assets/image (1) (1) (1).png>)
