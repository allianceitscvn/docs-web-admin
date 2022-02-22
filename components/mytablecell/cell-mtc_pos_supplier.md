---
description: Ô show vùng Khách Hàng
---

# Cell: mtc\_pos\_supplier

## Nút Customer Credit ($)

### Logic

* Cấu hình ở: **more.mtc\_pos\_supplier**
  * fLink: config field lấy link (có giá trị mới là link còn không thì vẫn là icon)
  * targetLink: config window mở link (mặc định: \_blank)



## Nút Add WhiteList / Remove WhiteList

### Logic

* Thêm bên trái nút Thêm Khách Hàng
* row.btn\_AddCustomerWhiteList = string.IsNullOrEmpty --> ko show nút add white list
* row.btn\_RemoveCustomerWhiteList = string.IsNullOrEmpty --> ko show nút remove white list
* Cấu hình button ở more.buttonAddWhiteList và more.buttonRemoveWhiteList
* Cấu hình api ở more.buttonAddWhiteList.api

## Task liên quan

* [POS-3049](https://allianceitscvn.atlassian.net/browse/POS-3049)
* [POS-3040](https://allianceitscvn.atlassian.net/browse/POS-3040)

## More

mtc\_pos\_supplier

* configCustomerCredit

buttonAddWhiteList

buttonRemoveWhiteList

