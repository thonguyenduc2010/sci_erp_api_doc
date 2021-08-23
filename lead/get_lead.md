***Lấy thông tin Lead***
----
 Lấy thông tin 1 Booking

* **URL**
  - Lấy thông tin Lead qua ID Lead: <br/>
   /{domain}/api/v1/lead/{id} <br/>
* **Method:**
  
  `GET`
  
*  **URL Params**

   /{domain}/api/v1/booking/1

* **Success Response:**
  
  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** 
    ```buildoutcfg 
    {
    "error": 0,
    "message": "Success",
    "data": {
        "id": 818635,
        "name": "Nguyễn Văn A",
        "contact_name": "Nguyễn Văn A",
        "gender": "male",
        "pass_port": false,
        "phone": "0123456789",
        "mobile": "0123456789",
        "birth_date": "1999-06-02",
        "year_of_birth": "1999",
        "email_from": "sondoan026@gmail.com",
        "country_id": 1,
        "country_name": "Andorra",
        "state_id": 7,
        "state_name": "Victoria",
        "district_id": false,
        "district_name": false,
        "street": "11 Tô Vĩnh Diện",
        "company_id": 2,
        "company_name": "BỆNH VIỆN KANGNAM HÀ NỘI",
        "facebook_acc": "Nguyễn Văn A",
        "send_info_facebook": false,
        "zalo_acc": "0123456789",
        "send_info_zalo": false,
        "brand_id": 1,
        "brand_name": "Kangnam",
        "price_list_id": 1,
        "price_list_name": "Bảng giá niêm yết Kangnam 2021",
        "category_source_id": 1,
        "category_source_name": "MARKETING",
        "overseas_vietnamese": "no",
        "work_online": "no",
        "online_counseling": "no",
        "shuttle_bus": "no",
        "campaign_id": 21,
        "campaign_name": "sss",
        "amount_total": 220000000.0,
        "create_on": "23-08-2021 03:13:48",
        "crm_line_ids": [
            {
                "id": 21511,
                "service_id": 5562,
                "service_name": "Combo Chỉnh hàm hô móm 2 hàm + Trượt cằm",
                "quantity": 1,
                "source_extend_id": 1,
                "source_extend_name": "Search engine",
                "total_before_discount": 150000000.0,
                "total_after_discount": 0
            },
            {
                "id": 21512,
                "service_id": 2282,
                "service_name": "Xóa hình xăm có sẹo  - Mức 10 (>700cm) (Giá tính trên hình)",
                "quantity": 1,
                "source_extend_id": 1,
                "source_extend_name": "Search engine",
                "total_before_discount": 70000000.0,
                "total_after_discount": 0
            }
        ]
    }
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
