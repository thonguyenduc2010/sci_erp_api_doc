***Lấy thông tin 1 khách hàng***
----
  Chi tiết về 1 khách hàng như lịch sử sử dụng dịch vụ, chân dung khách hàng, booking

* **URL**

   /{domain}/api/v1/account

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/account?phone=091231212

   **Required:**
 
   `phone=[string]` 
   -Số điện thoại của khách hàng
    | Attribute  | Method  | Type  | Description  |   |
    |---|---|---|---|---|
    | phone | GET  | string  | Số điện thoại của khách hàng  |   |
    |   |   |   |   |   |
    |   |   |   |   |   |

* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** `{ id : 12 }`
 
* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**

  <_Just a sample call to your endpoint in a runnable format ($.ajax call or a curl request) - this makes life easier and more predictable._> 

* **Notes:**

  <_This is where all uncertainties, commentary, discussion etc. can go. I recommend timestamping and identifying oneself when leaving comments here._> 
