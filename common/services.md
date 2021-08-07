
***1.2 Danh sách dịch vụ***
----

* **URL**

    
    /{domain}/api/v1/services


* **Method:**

  
    `GET`

  
* **Data Params**


  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | code| string  | Mã dịch vụ | | |
  | name| string  | Tên dịch vụ | | |
  | institution_ids | list | Cơ sở y tế | | Danh sách ID cơ sở y tế có sử dụng dịch vụ |
  | service_department_ids | list  | Khoa thực hiện | | Danh sách ID khoa thực hiện dịch vụ |
  | service_room_ids| list  | Phòng thực hiện | | Danh sách ID phòng thực hiện dịch vụ |

* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
    `{` <br />
	`'id': 28284,`  <br />
   ` 'code': 'KNPTBMM0001',` <br />
	`'name': 'Bấm mí Hàn Quốc',` <br />
	`'institution_ids': [11, 13],` <br />
	`'service_department_ids': [83, 87],` <br />
	`'service_room_ids': [60, 36],` <br />
    `} `<br />
      

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
