# Bill Detail



<details>

<summary><mark style="color:green;">Card Master</mark></summary>

![](<../../../.gitbook/assets/image (1).png>)

1. Header
   * Icon check
   * Icon card
     * Field: **PaymentTypeId**, **IsTransferBank**, **Transfer\_Text**
     * Logic
       * Đk show: **PaymentTypeId** = **2 hoặc 12**&#x20;
       * Màu sắc:
         * Xanh: **IsTransferBank = true**
         * Đỏ: **IsTransferBank = false**
       * **Transfer\_Text:** hiển thị tooltip khi nhấn vào
   * Mã đơn hàng
     * Field: **IONumber**
   * HTTT:
     * Field: **PaymentTypeDescription**
2. Middle
3. Footer

</details>

<details>

<summary><mark style="color:purple;">Bottom Bar</mark></summary>

* Tạo bởi client
  * "Kiểm đơn"
  * "Giao hàng"
  * "Đã giao"
  * "Sự cố"
  * "Đã soạn xong"
* Lấy từ server
  * Field: **ListButtons**
  * Logic:&#x20;
    * Lọc danh sách chỉ lấy button có api chứa **Bill/BillPayment\_CK** hoặc **Bill/BillPayment\_COD**

</details>
