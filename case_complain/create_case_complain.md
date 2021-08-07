***Tạo Case khiếu nại***
----
 **URL**

    /{domain}/api/v1/case
 **Method**

    `POST`
 **URL Params**
  
  *Complain Params*
  
  | Attribute  | Method  | Type  | Description  |  Required | Note |
  |---|---|---|---|---|---|
  | name | GET  | string  | Tên Case | x  |
  | subject_case | GET  | string  | Tiêu đề case | x  |
  | type_case | GET  | integer  | Loại case | x  | 1:Complain, 2:Warning |
  | receive_source | GET  | integer  | Nguồn tiếp nhận | x  | 1:Call center, 2:Email, 3:Inbox, 4:Directly |
  | phone | GET  | string  | Số điện thoại khách hàng | x  |
  | partner_id | GET  | integer  | Tên khách hàng |   | Danh sách khách hàng |
  | booking_id | GET  | integer  | Mã Booking |   |
  | phone_call_id | GET  | integer  | Mã PhoneCall |   |
  | user_id | GET  | string  | Người tiếp nhận | x  |
  | stage_id | GET  | integer  | Người tiếp nhận | x  | 1: Need, 2: Processing, 3:Finding more Information, 4:Waiting response, 5:Need to track, 6:Resolved, 7:Complete  |
  | brand_id | GET  | integer  | Thương hiệu | x  | Danh sách Thương hiệu |
  | company_id | GET  | integer  | Chi nhánh | x  | Danh sách Chi nhánh |
  | product_ids | GET  | integer  | Dịch vụ khiếu nại |   | Danh sách dịch vụ |
  | priority | GET  | integer  | Mức độ ưu tiên | x  | 1:Low, 2:Normal, 3:High, 4:Urgent |
  | content_complain_ids | GET  | integer  | Nội dung khiếu nại | x  | List các nội dung: _Content Params_ |
  | content_solution_ids | GET  | integer  | Giải pháp | x  | List các nội dung: _Solution Params_ |
  | note | GET  | string  | Ghi chú |   |  |

  *Content Params*
  
  | Attribute  | Method  | Type  | Description  |  Required | Note |
  |---|---|---|---|---|---|
  | Phòng ban | GET  | integer  | Phòng ban |   | Danh sách phòng ban |


  *Solutions Params*
  
  | Attribute  | Method  | Type  | Description  |  Required | Note |
  |---|---|---|---|---|---|
  | desc | GET  | string  | Phản ánh khách hàng |   |  |
  | solution | GET  | string  | Giải pháp |   |  |
