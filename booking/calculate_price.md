***Tính giá dịch vụ***
----
* **URL**

    /{domain}/api/v1/booking/canculate-price
    
 **Method**

    `GET`
* **URL Params**
  
  *Complain Params*
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | phone| string  | Điện thoại | x  | Số điện thoại Khách hàng |
  | price_list_id| integer  | Bảng giá | x  | |
  | service_ids | integer  | Dịch vụ | x  | Danh sách dịch vụ |
  | quantity | integer  | Số lượng | x  | Số lượng tương ứng đối với từng dịch vụ |
  | crm_discount_program| integer  | Chương trình khuyến mại |  | Danh sách Chương trình khuyến mại |
  | price| float  | Giá |  | Giá tạm tính từng dịch vụ _Trả về từ ERP_|
  | price_total| float  | Tổng giá |  | Tổng giá tạm tính _Trả về từ ERP_|

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

