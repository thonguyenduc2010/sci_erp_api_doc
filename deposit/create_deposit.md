***Danh sách khiếu nại***
----
 **URL**

    8.2: Tạo phiếu đặt cọc
    /{domain}/api/v1/crm_request_deposit/create
 **Method**

    `POST`
 **URL Params**
  
  *Complain Params*
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | booking_id| integer  | Booking | x  | Booking còn hiệu lực |
  | partner_id | integer  | Khách hàng | x  | Lấy từ danh sách KH  |
  | brand_id| integer  | Thương hiệu |  x | Lấy từ danh sách thương hiệu |
  | company_id| integer  | Chi nhánh | x  | Lấy từ danh sách chi nhánh |
  | date| date  | Ngày | x  | Định dạng _Y-M-D_ |
  | payment_method| integer  | Phương thức thanh toán | x  | 1:Tiền mặt, 2: Chuyển khoản, 3:Thanh toán nội bộ, 4:Quẹt thẻ qua POS, 5:Thanh toán qua ví điện tử|
  | currency_id| integer  | Tiền tệ |   | 1: EUR, 2:USD, 3:VND .Nếu  không có, hệ thống tự chọn là 3:VND|
  | amount| float  | Số tiền | x  | |
  | journal_id| integer  | Sổ nhật ký | x  | Lấy từ danh sách sổ nhật ký |
  | note| string  | Nội dung đặt cọc | x   |  |

**Phản hồi thành công:**

  * **Code:** 200 <br />
    **Content:** `{ id : ,}`
  * 
**Lỗi:**

  <_Thiếu các trường bắt buộc_>

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Missing required field value" }`