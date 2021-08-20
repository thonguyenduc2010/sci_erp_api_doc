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
 
    | Tham số  | Tính bắt buộc  | Kiểu dữ liệu  | Mô tả  |
    |---|---|---|---|
    | phone | yes  | string  | Số điện thoại của khách hàng  |


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
        "street2": "",
        "country_id": 241,
        "country_name": "Việt Nam",
        "state_id": 1070,
        "state_name": "Hà Nội",
        "contact_address": "16 ngõ 71 phố Tân Ấp, Ba Đình\n\n\nHà Nội Việt Nam",
        "email": "nguyenhuulinhbk@gmail.com",
        "birth_date": "1990-09-09",
        "year_of_birth": "1990",
        "age": 31,
        "gender": "male",
        "code_customer": "CUS276780",
        "price_list": [
            {
                "id": 1,
                "name": "Bảng giá niêm yết Kangnam 2021"
            }
        ],
        "bookings": [
            {
                "id": 818567,
                "name": "Book-687598",
                "booking_date": "2021-08-09 08:11:13"
            },
            {
                "id": 818538,
                "name": "Book-687584",
                "booking_date": "2021-08-15 01:34:39"
            },
            {
                "id": 818105,
                "name": "Book-687358",
                "booking_date": "2021-07-14 17:00:00"
            },
            {
                "id": 817480,
                "name": "Book-687099",
                "booking_date": "2021-05-27 03:41:49"
            },
            {
                "id": 817353,
                "name": "Book-687041",
                "booking_date": "2021-06-20 01:55:14"
            },
            {
                "id": 817352,
                "name": "Book-687040",
                "booking_date": "2021-06-19 01:36:07"
            },
            {
                "id": 817315,
                "name": "Book-687023",
                "booking_date": "2021-06-17 10:09:16"
            },
            {
                "id": 817306,
                "name": "Book-687019",
                "booking_date": "2021-06-30 03:03:26"
            },
            {
                "id": 817302,
                "name": "Book-687017",
                "booking_date": "2021-06-17 04:13:22"
            },
            {
                "id": 817296,
                "name": "Book-687014",
                "booking_date": "2021-06-17 02:13:00"
            },
            {
                "id": 817286,
                "name": "Book-687009",
                "booking_date": "2021-06-16 10:05:39"
            }
        ],
        "cases": [],
        "examinations": [
            {
                "id": 8521,
                "name": "PK-2021-002726",
                "date": "2021-07-15",
                "department_id": 14,
                "department_name": "Phòng Khám Răng Hàm Mặt",
                "services": [
                    "Phẫu thuật chỉnh hàm hô móm kết hợp niềng răng mức 1",
                    "Răng sứ Venus gắn trên răng sứ cố định",
                    "Trụ Implant Korea chất lượng (Dentium)"
                ]
            },
            {
                "id": 8297,
                "name": "PK-2021-002550",
                "date": "2021-06-23",
                "department_id": 12,
                "department_name": "Phòng Khám Laser",
                "services": [
                    "Điều trị nám bằng Picosure Mức 2"
                ]
            },
            {
                "id": 8288,
                "name": "PK-2021-002544",
                "date": "2021-06-23",
                "department_id": 12,
                "department_name": "Phòng Khám Laser",
                "services": [
                    "Điều trị nám bằng Picosure Mức 2"
                ]
            },
            {
                "id": 8201,
                "name": "PK-2021-002502",
                "date": "2021-06-19",
                "department_id": 12,
                "department_name": "Phòng Khám Laser",
                "services": [
                    "Điều trị nám bằng Laser Toning Mức 1"
                ]
            },
            {
                "id": 8170,
                "name": "PK-2021-002474",
                "date": "2021-06-17",
                "department_id": 12,
                "department_name": "Phòng Khám Laser",
                "services": [
                    "Điều trị nám bằng Laser Toning Mức 1",
                    "Điều trị nám bằng Picosure Mức 2"
                ]
            },
            {
                "id": 8168,
                "name": "PK-2021-002472",
                "date": "2021-06-17",
                "department_id": 8,
                "department_name": "Phòng Khám PTTM",
                "services": [
                    "Cấy mỡ 1 vùng má/ Thái dương/ Rãnh mũi má/ Môi trên/ Môi dưới/ Môi lớn +bé"
                ]
            },
            {
                "id": 8162,
                "name": "PK-2021-002466",
                "date": "2021-06-17",
                "department_id": 12,
                "department_name": "Phòng Khám Laser",
                "services": [
                    "Trị sẹo bằng Laser mức 1 - 1 vùng"
                ]
            },
            {
                "id": 8156,
                "name": "PK-2021-000005",
                "date": "2021-06-16",
                "department_id": 146,
                "department_name": "Phòng Khám Răng Hàm Mặt",
                "services": [
                    "Phẫu thuật chỉnh hàm hô móm kết hợp niềng răng mức 1"
                ]
            }
        ],
        "loyalty_cards": [
            {
                "id": 426,
                "name": false,
                "rank": "",
                "date_interaction": "2021-06-17 02:36:28",
                "validity_card": 0,
                "due_date": "2021-06-17 02:36:28"
            }
        ],
        "customer_personas": {
            "desires": [],
            "pain_point": []
        },
        "orders": [
            {
                "id": 11097,
                "name": "SO11097",
                "amount_total": 84600000,
                "state": "draft",
                "create_date": "2021-07-15 08:39:58"
            },
            {
                "id": 10775,
                "name": "SO10775",
                "amount_total": 6000000,
                "state": "done",
                "create_date": "2021-06-23 09:42:23"
            },
            {
                "id": 10766,
                "name": "SO10766",
                "amount_total": 6000000,
                "state": "done",
                "create_date": "2021-06-23 03:00:20"
            },
            {
                "id": 10676,
                "name": "SO10676",
                "amount_total": 1800000,
                "state": "done",
                "create_date": "2021-06-19 01:37:58"
            },
            {
                "id": 10631,
                "name": "SO10631",
                "amount_total": 3600000,
                "state": "done",
                "create_date": "2021-06-17 10:10:53"
            },
            {
                "id": 10629,
                "name": "SO10629",
                "amount_total": 1000000,
                "state": "done",
                "create_date": "2021-06-17 03:11:13"
            },
            {
                "id": 10623,
                "name": "SO10623",
                "amount_total": 1800000,
                "state": "done",
                "create_date": "2021-06-17 02:36:28"
            },
            {
                "id": 10613,
                "name": "SO10613",
                "amount_total": 1000000,
                "state": "draft",
                "create_date": "2021-06-16 10:21:31"
            }
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


