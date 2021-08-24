***Lấy thông tin Booking***
----
 Lấy thông tin 1 Booking

* **URL**
  - Lấy thông tin Booking qua ID Booking: <br/>
   /{domain}/api/v1/booking/{id} <br/>
  - Lấy thông tin Booking qua mã Booking: <br/>
  /{domain}/api/v1/booking-name/{name}
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

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** 
    ```
    {
      "type": "access_token",
      "message": "token seems to have expired or invalid"
    }

    ```

* **Sample Call:**


* **Notes:**
