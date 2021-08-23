***Lấy thông tin Booking***
----
 Lấy thông tin 1 Booking

* **URL**
  - Lấy thông tin Booking qua ID Booking: <br/>
   /{domain}/api/v1/booking/{id} <br/>
  - Lấy thông tin Booking qua mã Booking: <br/>
  /{domain}/api/v1/booking/{name}
* **Method:**
  
  `GET`
  
*  **URL Params**

   /{domain}/api/v1/booking/1 <br/>
   /{domain}/api/v1/booking/Book-687629
   

* **Success Response:**
  
  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** 
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
