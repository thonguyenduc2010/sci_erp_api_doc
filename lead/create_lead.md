***Tạo Lead***
----
 Tạo Lead

* **URL**

  /{domain}/api/v1/lead

* **Method:**
  
  `POST`
  
*  **URL Params**

   /{domain}/api/v1/lead
    | Attribute  | Require  | Type  | Description |
    |---|---|---|---|
    | phone | True  | string  | Số điện thoại của khách hàng |
    |   |   |   |   |   |
    |   |   |   |   |   |

* **Success Response:**
  
  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** `{ id : 12,
    date: '2001-08-01'
    }`
 
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
