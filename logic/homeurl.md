# HomeURL

Khi cần chuyển về home, lấy từ HCF.home\_url ra để redirect

## Flow hiện tại

### Chưa Login

* Gọi FirstSetting
  * Lấy DefaultHomeURL  -> set HCF.home\_url, lưu localStorage: HomeURL
* Sau khi login
  * Lưu AuthInfo vào LocalStorage: Auth-Info
  * Parse AuthInfo, lấy home\_url -> set HCF.home\_url, lưu LocalStorage: HomeURL

### Đã login

* Parse AuthInfo -> set HCF.home\_url, lưu LocalStorage: HomeURL
* Gọi FirstSetting
  * Lấy DefaultHomeURL  -> set HCF.home\_url, lưu localStorage: HomeURL

## Sử dụng

* Sau khi login -> open Home Page
* Click logo -> open Home Page

## Vấn đề

### Vấn đề 1

A login với home page /p1 -> cần đổi sang /p2 mà ko cần logout->login

Giải quyết:

### Vấn đề 2

Ngưng sử dụng home page cho toàn bộ user hoặc user cụ thể
