
***1.2 Danh sách dịch vụ***
----

* **URL**

    
   `GET` Lấy danh sách dịch vụ `/{domain}/api/v1/services`

   `GET` Lấy chi tiết danh sách dịch vụ theo ID `/{domain}/api/v1/services/{id}`


* **Method:**

  
    `GET`

* **Url Params**


  | Attribute| Type | Description |
  |---|---|---|
  | id | string  | Danh sách dịch vụ của ID |
  | brand | boolean  | Có/Không lọc theo thương hiệu |


* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
    `{` <br />
	`'id': 28284,`  <br />
   ` 'code': 'KNPTBMM0001',` <br />
	`'name': 'Bấm mí Hàn Quốc',` <br />
    `} `<br />
      

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
