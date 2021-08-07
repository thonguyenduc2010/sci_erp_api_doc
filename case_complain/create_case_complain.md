***Tạo và cập nhật Case khiếu nại***
----
 **URL**

    /{domain}/api/v1/crm.case
    /{domain}/api/v1/crm.case?id={int}
 **Method**

    `GET|POST`
 **URL Params**
  
  *Complain Params*
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | name | string  | Tên Case | x  |
  | complain_group_id| integer  | Nhóm khiếu nại | x  | Danh sách nhóm khiếu nại  _model:crm.complain.group_ |
  | complain_id| integer  | Nội dung khiếu nại | x  | Danh sách khiếu nại  _model:crm.complain_ |
  | type_case| integer  | Loại case | x  | 1:Complain, 2:Warning |
  | start_date| datetime  | Ngày giờ bắt đầu/tiếp nhận | x  | Mặc định là thời gian hiện tại tại thời điểm tạo case |
  | receive_source| integer  | Nguồn tiếp nhận | x  | 1:Call center, 2:Email, 3:Inbox, 4:Directly |
  | phone| string  | Số điện thoại khách hàng | x  |
  | partner_id| integer  | Tên khách hàng |   | Danh sách khách hàng |
  | booking_id| integer  | Mã Booking |   |
  | phone_call_id| integer  | Mã PhoneCall |   |
  | user_id| id  | Người tiếp nhận | x  |   |
  | stage_id| integer  | Người tiếp nhận | x  | 1: Need, 2: Processing, 3:Finding more Information, 4:Waiting response, 5:Need to track, 6:Resolved, 7:Complete  |
  | brand_id| integer  | Thương hiệu | x  | Danh sách Thương hiệu |
  | company_id| integer  | Chi nhánh | x  | Danh sách Chi nhánh |
  | product_ids| integer  | Dịch vụ khiếu nại |   | Danh sách dịch vụ |
  | priority| integer  | Mức độ ưu tiên | x  | 1:Low, 2:Normal, 3:High, 4:Urgent |
  | content_solution_ids| integer  | Giải pháp | x  | List các nội dung: _Solution Params_ |
  | note| string  | Ghi chú |   |  |
  | create_by| integer  | Người tạo case | x  |  |


  *Solutions Params*
  
  | Attribute  | Method  | Type  | Description  |  Required | Note |
  |---|---|---|---|---|---|
  | desc| string  | Phản ánh khách hàng |   |  |
  | solution| string  | Giải pháp |   |  |
