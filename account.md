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
    "data": {
        "id": 513611,
        "name": "NGUYỄN HỮU LINH",
        "street": "16 ngõ 71 phố Tân Ấp, Ba Đình",
        "street2": false,
        "country_id": [
            241,
            "Việt Nam"
        ],
        "state_id": [
            1070,
            "Hà Nội (VN)"
        ],
        "contact_address": "16 ngõ 71 phố Tân Ấp, Ba Đình\n\n\nHà Nội Việt Nam",
        "email": "nguyenhuulinhbk@gmail.com",
        "birth_date": "1990-09-09",
        "year_of_birth": "1990",
        "age": 31,
        "gender": "male",
        "code_customer": "CUS276780",
        "invoice_ids": [
            1111,
            1110,
            802,
            722,
            694,
            691,
            697
        ],
        "opportunity_ids": [
            818105,
            817480,
            817353,
            817352,
            817315,
            817306,
            817302,
            817296,
            817286
        ],
        "sale_order_count": 8,
        "sale_order_ids": [
            11097,
            10775,
            10766,
            10676,
            10631,
            10629,
            10623,
            10613
        ],
        "crm_ids": [
            818105,
            818103,
            817480,
            817479,
            817353,
            817352,
            817351,
            817315,
            817314,
            817306,
            817305,
            817302,
            817301,
            817296,
            817295,
            817286,
            817285
        ],
        "pricelist": [
            1,
            "Bảng giá niêm yết Kangnam 2021 (VND)"
        ]
    }
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


