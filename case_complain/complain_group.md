***Danh sách nhóm khiếu nại***
----
 **URL**

    /{domain}/api/v1/crm-complain-group
 **Method**

    `GET`
 **URL Params**
  
  *Complain Params*
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | name | string  | Tên Case | x  | Tên nhóm khiếu nại |

**Phản hồi thành công:**
  
  * _Hệ thống sẽ trả lại danh sách các nhóm khiếu nại có trên hệ thống ERP_

    * **Code:** 200 <br />
      **Content:** `{ id : ,name: ' '}