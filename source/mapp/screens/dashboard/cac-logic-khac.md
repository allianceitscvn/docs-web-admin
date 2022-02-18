# Các logic khác



* <mark style="color:orange;">**Khi quét QR code:**</mark>&#x20;
  * Url:  /mhome?QRCode=695ecdc6-d31b-4609-b3f4-eb92d0082d1a
  * Logic:
    * Sau khi quét thì sẽ mở trang home với url như trên
    * Gọi api MyDashboard
    * Kiểm tra field: Config/EntityScreen = "BillDetail" -> Chuyển tới trang detail
