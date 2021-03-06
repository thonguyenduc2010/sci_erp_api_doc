# Tài liệu API 
## Mô tả
## Xác thực (Authorization)

- Xác thực qua access token, yêu cầu tất cả các request gọi lên đều phải thêm "access-token" header
- Ví dụ:

POST: /{domain}/api/v1/lead

```
Header:
  access-token: {access_token}
  aontent-type: application/x-www-form-urlencoded
  charset: utf-8
```

## 1. Common
  ### [1.1. Danh sách Thương hiệu](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/brand.md)
  ### [1.2. Danh sách Cơ sở](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/location.md)
  ### [1.3. Danh sách Dịch vụ](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/services.md)
  ### [1.4. Danh sách Khuyến Mãi](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/promotion.md)
  ### [1.5. Danh sách Bảng giá](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/pricelist.md)
  ### [1.6. Danh sách Chiến dịch](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/campaign.md)
  ### [1.7. Danh sách Phòng ban](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/department.md)
  ### [1.8. Danh sách Quốc gia](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/countries.md)
  ### [1.9. Danh sách Tỉnh thành](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/states.md)
  ### [1.10.Danh sách Quận huyện](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/districts.md)
  ### [1.11.Danh sách Trạng thái](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/stage.md)
  ### [1.12.Danh sách Nhóm nguồn](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/source_category.md)
  ### [1.13.Danh sách Nguồn](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/source.md)
  ### [1.14.Danh sách Nhóm dịch vụ](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/common/service_categories.md)
  
## 2. Lead
### [2.1. Tạo lead](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/lead/create_lead.md)
### [2.2. Cập nhật lead](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/lead/update_lead.md)
### [2.2. Lấy thông tin lead](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/lead/get_lead.md)
  
## 3. Booking
### [3.1. Tính giá dịch vụ](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/calculate_price.md)
### [3.2. Tạo booking](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/create_booking.md)
### [3.3. Cập nhật booking](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/update_booking.md)
### [3.4. Lấy thông tin booking qua ID booking](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/booking/get_booking_by_id.md)

## 4. Account
  * [4.1. Lấy thông tin 1 khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account.md)
  * [4.2. Danh sách nhân sự](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/employee.md)
  * [4.3. Lấy thông tin cá nhân của khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account/personal_information.md)
  * [4.4. Lấy thông tin chân dung khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account/customer-portrait.md)
  * [4.5. Lấy danh sách bản ghi Lead của khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account/leads.md)
  * [4.6. Lấy danh sách bản ghi Booking của khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account/bookings.md)
  * [4.7. Lấy danh sách bản ghi Phone Call của khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account/phone_call.md)
  * [4.8. Lấy danh sách bản ghi Phiếu khám của khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account/walkin.md)
  * [4.9. Lấy thông tin thẻ thành viên của khách hàng](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/account/loyalty.md)
## 5. Phonecall
### [5.1. Tạo phonecall](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/phonecall/create_phonecall.md)
### [5.2. Danh sách type phone call](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/phonecall/type_phone_call.md)
### [5.2. Cập nhật phone call](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/phonecall/update_phonecall.md)
  
## 6. SMS
  * Đẩy thông tin sang Caresoft

## 7. Case Khiếu nại
### [7.1. Danh sách nhóm khiếu nại](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/case_complain/complain_group.md)
### [7.2. Danh sách khiếu nại](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/case_complain/complain.md)
### [7.3. Tạo case khiếu nại](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/case_complain/create_case_complain.md)

## 8. Phiếu đặt cọc
### [8.1. Danh sách sổ nhật ký](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/deposit/get_journal_id.md)
### [8.2. Tạo phiếu đặt cọc](https://github.com/thonguyenduc2010/sci_erp_api_doc/blob/main/deposit/create_deposit.md)
