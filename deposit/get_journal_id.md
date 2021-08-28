***Lấy ra danh sách các sổ  nhật ký phục vụ cho tạo phiếu đặt cọc***
----

**URL**

    8.1 Danh sách các sổ nhật ký
    /{domain}/api/v1/account-journal
**Method:**
  
  `GET`

 **URL Params**
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | company_id | integer  | Chi nhánh |   | Danh sách chi nhánh  |
  | payment_method | integer  | Phương thức thanh toán |   | 1:Tiền mặt, 2: Chuyển khoản, 3:Thanh toán nội bộ, 4:Quẹt thẻ qua POS, 5:Thanh toán qua ví điện tử  |

   

**Phản hồi thành công:**
  
  * _Hệ thống sẽ trả lại danh sách các sổ nhật ký có trên hệ thống ERP_
  * _Ngoài ra  nếu đầu vào còn cho biết CHI NHÁNH và PHƯƠNG THỨC THANH TOÁN, ERP cũng lọc bớt các sổ nhật ký và trả về các sổ phù hợp_

    * **Code:** 200 <br />
      **Content:** `{ id : ,name: ' '}`
    

