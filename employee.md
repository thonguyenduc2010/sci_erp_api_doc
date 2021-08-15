
***Danh sách Danh sách nhân sự***
----

* **URL**

  /{domain}/api/v1/employee

* **Method:**
  
    `GET`
  
*  **URL Params**

    | Tham số  | Tính bắt buộc  | Kiểu dữ liệu  | Mô tả  |
    |---|---|---|---|
    | company_id | yes  | Integer  | Id của cơ sở  |
    | deparment_id | yes  | Integer  | Id của phòng ban  |
    | limit | no  | Integer  | Số lượng bản ghi  |
    | offset | no  | Integer  | Thứ tự bản ghi được lấy  |
    

* **Success Response:**
  
    * **Code:** 200 <br />
    **Content:** 
    
    ```

      
    ```
 
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
```

```
* **Notes:**

