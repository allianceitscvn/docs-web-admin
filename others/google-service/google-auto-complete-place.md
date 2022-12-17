# Google Auto Complete Place

## Sử dụng API AutoComplete Place

* Vào trang https://console.cloud.google.com/google/maps-apis/api-list?referrer=search\&project=projectname
  * Bật Maps JavaScript API
  * Bật Places API
  * Bật Geocoding API:&#x20;
    * Để lấy thêm thông tin từ placeId
* Vào trang quản lý API: https://console.cloud.google.com/apis/credentials?project=projectname
  * Config OAuth consent screen nếu chưa đc config bao giờ
  * Create new credentials: API Key
    * Application restrictions: Nếu cần
      * None: Ai sử dụng cũng được
      * HTTP referers: Giới hạn website được phép sử dụng
    * Api Restrict: Map and Place
* Sử dụng: API Key

## Bổ sung thêm domain vào API Key đã có

* Vào trang quản lý API: [https://console.cloud.google.com/apis/credentials?project=projectname](https://console.cloud.google.com/apis/credentials?project=projectname)
* Vào Api Key cần bổ sung thêm domain
  * Add thêm domain
  * Chờ đợi để xác thực hoàn thành
