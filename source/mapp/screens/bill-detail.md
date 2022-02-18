# Bill Detail

<details>

<summary>Card Master</summary>

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
     * Field: IONumber
   * HTTT:
     * Field: **PaymentTypeDescription**
2. Middle
3. Footer

</details>

<details>

<summary>Bottom Bar</summary>

* Tạo bởi client
  * "Kiểm đơn"
  * "Giao hàng"
  * "Đã giao"
  * "Sự cố"
  * "Đã soạn xong"
* Lấy từ server
  * Field: **ListButtons**
  * Logic:&#x20;
    * Có field thì show hết các button trong field
    * Đối với user là quản lý thì chỉ gắn các button mà client chưa có

</details>
