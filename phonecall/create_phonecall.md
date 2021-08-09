
*** Tạo Phonecall ***
----
 Tạo Phonecall

* **URL**

  /{domain}/api/v1/phonecall

* **Method:**
  
  `POST`
  
*  **URL Params**

   /{domain}/api/v1/lead
    | Attribute  | Require  | Type  | Note | Description |
    |---|---|---|---| ---|
    | phone | True  | String  | | Số điện thoại của khách hàng |


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

