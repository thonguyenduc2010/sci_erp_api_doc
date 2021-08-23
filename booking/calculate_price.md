***Tính giá dịch vụ***
----
* **URL**

    /{domain}/api/v1/booking/calculate-price
    
 **Method**

    `GET`
* **URL Params**
  
  *Complain Params*
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | crm_line_ids| Mảng  | Danh sách dịch vụ (Được đánh số thứ tự) | x | [ <br/> { <br/> 'ordinal_numbers': 1,,<br/> 'service_id': id, <br/> 'quantity': Int, <br/> }, <br/> { <br/> 'ordinal_numbers': 2,,<br/> 'service_id': id, <br/> 'quantity': Int, <br/> } ] <br/> - ordinal_numbers: STT của line dịch vụ <br/> - service_id: Sản phẩm <br/>- quantity: Số lượng <br/>   |
  | crm_discount_program| integer  | Chương trình khuyến mại | x | Danh sách Chương trình khuyến mại |

* **Phản hồi thành công:**

  * **Code:** 200 <br />
    **Content:** `{ price : ,
    price_total: 
    }`
 
* **Lỗi:**
    
  <_Không tìm thấy khách hàng có số điện thoại yêu cầu trên hệ thống_>

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Phone Invalid" }`
  
  <_Số lượng của từng dịch vụ nhập vào không hợp lệ_>

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Quantity Invalid" }`

  <_Dịch vụ không nằm trong bảng giá hiện hành_>

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Service is not included in the current price list" }`

