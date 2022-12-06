# Logic

Start

* Remove localstorage
* Lưu localstorage: statuc check
* Lưu thời điểm idle vào localstorage
* Status: Check
* Tạo event mousemove

Cứ 1s Đếm thời gian khi di chuyển chuột

* Có di chuyển -> Update thời gian idle mới vào localstorage
  * Nếu Status khác Check
    * Expired: reload window
    * Countdown: show countdown với countdown remain từ localstorage
* Không di chuyển -> Nếu thời gian kiểm > thời điểm idle -> show modal countdown
  * Status: Countdown
  * Bắt đầu countdown 60s
  * Mỗi 1s đi update thời gian countdown
    * Nếu Status khác Countdown
      * Expred: reload window
    * Nếu hết thời gian -> tự động logout
    * Status: Expired

