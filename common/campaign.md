
***1.6 Danh sách chiến dịch***
----

* **URL**

    `GET` Danh sách chiến dịch: 
    `/{domain}/api/v1/campaign`
  
    `GET` Chi tiết danh sách chiến dịch theo ID: 
    `/{domain}/api/v1/campaign/<id>`
    
    `GET` Chi tiết thông tin chiến dịch: 
    `/{domain}/api/v1/campaign-item`
  
   
  
* **Method:**

  
    `GET`

* **Url Params**


  | Method | Attribute| Type | Description |
  |---|---|---|---|
  | `GET` | id | int  | ID Chiến dịch |
 


* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
  
`GET` Danh sách chiến dịch: 
    `/{domain}/api/v1/campaign`
  
      
    "count": 2,
    "data": [
        {
            "id": 24,
            "name": "NGÀY VÀNG HỘI THẢO T6/2021",
            "brand_id": [
                3,
                "Paris"
            ],
        },
        {
            "id": 11,
            "name": "HỘI CHỈNH NHA NIỀNG RĂNG",
            "brand_id": [
                3,
                "Paris"
            ],
        }]
      

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
