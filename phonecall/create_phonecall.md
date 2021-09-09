
*** Tạo Phonecall ***
----
 Tạo Phonecall

* **URL**

  /{domain}/api/v1/phone-call

* **Method:**
  
  `POST`
  
*  **URL Params**

    | Attribute  | Require  | Type  | Note | Description |
    |---|---|---|---| ---|
    | phone | True  | String  | | Số điện thoại của khách hàng |
    | type_phonecall | True | Int | Sử dụng API lấy danh sách loại phone call | Loại phone call |
    | direction | True | Stirng | 'in' - Gọi vào; 'out' - Gọi ra | Hướng gọi |


* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** `{ id : 12,
    date: '2001-08-01'
    }`
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**

* **Notes:**

