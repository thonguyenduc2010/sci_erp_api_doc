***Tính giá dịch vụ***
----
* **URL**

    /{domain}/api/v1/booking/calculate-price
    
 **Method**

    `GET`
* **URL Params**
  
  *Complain Params*
  
  | Attribute| Type  | Description  |  Required | Note |
  |---|---|---|---|---|
  | price_list_id| integer  | Bảng giá | x |  |
  | crm_line_ids| Mảng  | Danh sách dịch vụ (Được đánh số thứ tự) | x | [ <br/> { <br/> 'ordinal_numbers': 1,,<br/> 'product_id': id, <br/> 'quantity': Int, <br/> }, <br/> { <br/> 'ordinal_numbers': 2,,<br/> 'product_id': id, <br/> 'quantity': Int, <br/> } ] <br/> - ordinal_numbers: STT của line dịch vụ <br/> - product_id: Sản phẩm <br/>- quantity: Số lượng <br/>   |
  | crm_discount_program| integer  | Chương trình khuyến mại | x | Danh sách Chương trình khuyến mại |

* **Phản hồi thành công:**

  * **Code:** 200 <br />
    **Content:** `{
        'price_total': price_total - tổng giá,
        'crm_line_ids':[
                            {
                            'ordinal_numbers': số thứ tự,
                            'amount_after_discount': giá line dịch vụ sau khi giảm giá,
                            }
                        ]
        }`

