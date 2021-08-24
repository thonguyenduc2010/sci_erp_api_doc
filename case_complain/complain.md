***Danh sách khiếu nại***
----
 **URL**

    /{domain}/api/v1/crm-complain
    /{domain}/api/v1/crm-complain?complain_group={id}
 **Method**

    `GET`
 **URL Params**
  
  *Complain Params*
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | complain_group_id| integer  | Nhóm khiếu nại | x  | Danh sách nhóm khiếu nại |
  | name | string  | Tên Case | x  | Tên khiếu nại |
  | department_ids| integer  | Phòng ban |   | Danh sách phòng ban |

**Phản hồi thành công:**
  
  * _Hệ thống sẽ trả lại danh sách các khiếu nại có trên hệ thống ERP_

    * **Code:** 200 <br />
      **Content:** `{ id : ,name: ' '}