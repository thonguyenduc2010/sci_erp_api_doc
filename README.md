# Tài liệu API 
## Mô tả
## Xác thực (Authorization)

- Xác thực qua access token, yêu cầu tất cả các request gọi lên đều phải thêm "authorization" header
- Ví dụ:
POST: /{domain}/api/v1/lead
Header:
```
authorization: {access_token}
aontent-Type: application/x-www-form-urlencoded
charset: utf-8
```

## 1. Common
  ### [1.1. Danh sách Cơ sở](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/locationshop.md)
  ### [1.2. Danh sách Dịch vụ](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/service.md)
  ### [1.3. Danh sách Khuyến Mãi](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/promotion.md)
  ### [1.4. Danh sách Bảng giá](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/pricelist.md)
  ### [1.5. Danh sách Chiến dịch](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/campaign.md)
  ### [1.6. Danh sách Phòng ban](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/department.md)
  ### [1.7. Danh sách Quốc gia](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/countries.md)
  ### [1.8. Danh sách Tỉnh thành](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/states.md)

## 2. Lead
### [2.1. Tạo lead](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/lead/create_lead.md)
### [2.2. Cập nhật lead](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/lead/update_lead.md)
  
## 3. Booking
### [3.1. Tính giá dịch vụ](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/calculate_price.md)
### [3.2. Tạo booking](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/create_booking.md)
### [3.3. Cập nhật booking](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/update_booking.md)
### [3.4. Lấy thông tin booking qua ID booking](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/get_booking_by_id.md)

## 4. Account
  ### [4.1. Lấy thông tin 1 khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account.md)

## 5. Phonecall
### [5.1. Tạo phonecall](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/phonecall/create_phonecall.md)
  * Đẩy thông tin sang Caresoft
  
## 6. SMS
  * Đẩy thông tin sang Caresoft

## 7. Case Khiếu nại
### [7.1. Danh sách khiếu nại](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/case_complain/cases.md)
### [7.2. Tạo khiếu nại](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/case_complain/create_case_complain.md)
