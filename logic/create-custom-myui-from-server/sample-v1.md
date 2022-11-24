# Sample v1

Sample

```json
{
  "t": "t_div",
  "st": {
    "border": "0px",
    "padding": "0px",
    "fontSize": "11px"
  },
  "ch": [
    {
      "t": "t_div",
      "st": {
        "textAlign": "center",
        "fontSize": "18px"
      },v
      "ch": "Xuất bán sỉ"
    },
    {
      "t": "t_div",
      "ch": [
        {
          "t": "t_div",
          "ch": [
            "Số Phiếu: ",
            "fn/myData/IONumber"
          ]
        },
        {
          "t": "t_div",
          "ch": [
            "Ngày: ",
            "fn/myData/EnterDate_Text"
          ]
        },
        {
          "t": "t_div",
          "ch": [
            "KH: ",
            "fn/myData/SupplierName"
          ]
        }
      ]
    },
    {
      "t": "t_div",
      "ch": {
        "t": "t_table",
        "st": {
          "width": "100%",
          "fontSize": "11px",
          "marginTop": "10px",
          "marginBottom": "5px",
          "borderTop": "1px solid black",
          "borderBottom": "1px solid black",
          "borderCollapse": "collapse"
        },
        "p": {
          "th": [
            "Hàng hóa",
            "Đ.Giá",
            "SL"
          ],
          "thSt": [
            {
              "width": "75%",
              "textAlign": "left",
              "padding": "5px 0px"
            },
            {
              "width": "17%",
              "textAlign": "center",
              "padding": "5px"
            },
            {
              "width": "8%",
              "textAlign": "center",
              "padding": "5px"
            }
          ],
          "tr": "fn/myData/iostockDetails",
          "thStR": {
            "borderBottom": "1px solid black"
          },
          "trSt": [],
          "td": [
            "fn/myData/MaterialCode",
            "fn/myData/SellPrice",
            "fn/myData/Quantity"
          ],
          "tdSt": [
            {
              "textAlign": "left",
              "borderBottom": "1px solid black"
            },
            {
              "textAlign": "center",
              "borderBottom": "1px solid black"
            },
            {
              "textAlign": "center",
              "borderBottom": "1px solid black"
            }
          ],
          "fRB": {
            "colSpan": "3",
            "ch": "fn/myData/MaterialName"
          }
        }
      }
    }
  ]
}
```
