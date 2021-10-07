***Lấy thông tin cá nhân 1 khách hàng***
----
  Trả về thông tin cá nhân của khách hàng như: tên, tuổi, địa chỉ,....

* **URL**

   /{domain}/api/v1/account

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/account?phone=091231212&phone_2=01232812123&phone_3=01232812123

   **Required:**
 
    | Tham số  | Tính bắt buộc  | Kiểu dữ liệu  | Mô tả  |
    |---|---|---|---|
    | phone | yes  | string  | Số điện thoại của khách hàng  |
    | phone_2 | no  | string  | Số điện thoại 2 của khách hàng  |
    | phone_3 | no  | string  | Số điện thoại 3 của khách hàng  |


* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
```
  {
    "error": 0,
    "message": "Success",
    "data": {
        "id": 410389,
        "name": "NGUYỄN HỮU LINH",
        "street": "16 NGÕ 71 PHỐ TÂN ẤP, P. PHÚC XÁ",
        "street2": "",
        "country_id": 241,
        "country_name": "Việt Nam",
        "state_id": 1070,
        "state_name": "Hà Nội",
        "contact_address": "16 NGÕ 71 PHỐ TÂN ẤP, P. PHÚC XÁ\n\n\nHà Nội Việt Nam",
        "email": "nguyenhuulinhbk@gmail.com",
        "phone": "0387548453",
        "mobile": false,
        "birth_date": "1990-09-09",
        "year_of_birth": "1990",
        "age": 31,
        "gender": "male",
        "code_customer": "CUS410350",
        "account_url": "http://localhost:13000/web#id=410389&action=553&model=res.partner&view_type=form&cids=0&menu_id=379"
    }
}
```
