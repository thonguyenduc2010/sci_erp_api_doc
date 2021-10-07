***Lấy thông tin chân dung khách hàng***
----
  Chi tiết về chân dung khách hàng

* **URL**

   /{domain}/api/v1/customer-portrait

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/account?phone=091231212&phone_2=01232812123&phone_3=01232812123

   **Required:**
 
    | Tham số  | Tính bắt buộc  | Kiểu dữ liệu  | Mô tả  |
    |---|---|---|---|
    | phone | yes  | string  | Số điện thoại của khách hàng  |
    | phone_2 | no  | string  | Số điện thoại 2 của khách hàng  |
    | phone_3 | no  | string  | Số điện thoại 3 của khách hàng  |


* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
```
{
    "error": 0,
    "message": "Success",
    "data": {
        "hobby": [],
        "revenue_source": false,
        "term_goals": false,
        "behavior_on_the_internet": false,
        "affected_by": false,
        "work_start_time": 0.0,
        "work_end_time": 0.0,
        "break_start_time": 0.0,
        "break_end_time": 0.0,
        "transport": false,
        "customer_personas": {
            "desires": [],
            "pain_point": []
        },
        "account_url": "http://localhost:13000/web#id=413242&action=553&model=res.partner&view_type=form&cids=0&menu_id=379"
    }
}
```

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

* **Sample Call:**



* **Notes:**
