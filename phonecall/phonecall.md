***Lấy danh sách phonecall của khách hàng***
----
  Danh sách các phonecall của 1 khách hàng qua số điện thoại

* **URL**

   /{domain}/api/v1/phonecall

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/phonecall?phone=091231212

   **Required:**
 
    | Tham số  | Tính bắt buộc  | Kiểu dữ liệu  | Mô tả  |   |
    |---|---|---|---|---|
    | phone | yes  | string  | Số điện thoại của khách hàng  |   |


* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
```
{
    "error": 0,
    "message": "Success",
    "count": 2,
    "data": [
      {"id":12312,},
      {"id":12313,}
    ]
    
}

```
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**



* **Notes:**



