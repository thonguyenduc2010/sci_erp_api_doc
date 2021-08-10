***1.1 Danh sách cơ sở***
----
  Danh sách tất cả cơ sở của công ty

* **URL**

  /{domain}/api/v1/location

* **Method:**

  `GET`
  
*  **URL Params**

* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
    ```
    {
    "error": 0,
    "message": "Success",
    "count": 28,
    "data": [
        {
            "id": 23,
            "code": "HH",
            "name": "BỆNH VIỆN HỒNG HÀ"
        },
        {
            "id": 2,
            "code": "HN",
            "name": "BỆNH VIỆN KANGNAM HÀ NỘI"
        },
        {
            "id": 3,
            "code": "HCM",
            "name": "BỆNH VIỆN KANGNAM HỒ CHÍ MINH"
        },
        {
            "id": 4,
            "code": "SG",
            "name": "BỆNH VIỆN KANGNAM SÀI GÒN"
        },
        {
            "id": 12,
            "code": false,
            "name": "BỆNH VIỆN THẨM MỸ ĐÔNG Á HỒ CHÍ MINH"
        },
        {
            "id": 25,
            "code": false,
            "name": "HỌC VIỆN THẨM MỸ SCI HÀ NỘI"
        },
        {
            "id": 24,
            "code": false,
            "name": "HỌC VIỆN THẨM MỸ SCI HỒ CHÍ MINH"
        },
        {
            "id": 18,
            "code": false,
            "name": "NHA KHOA PARIS 3/2"
        },
        {
            "id": 22,
            "code": false,
            "name": "NHA KHOA PARIS BÌNH DƯƠNG"
        },
    ]
}
    ```
 
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
