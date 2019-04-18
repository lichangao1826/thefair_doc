**简要描述** 

- 创建商品

**请求URL** 
- ` http://xxx/product/product/createProduct `
  
**请求方式**
- POST 

**请求参数** 

|参数名|必选|类型|说明|
|:----|:---|:---|:---|
|product_type|是|enum string|商品类型|
|product_short_name|是|string|商品名称|
|start_time|是|string|添加时间|
|publish_time|否|string|发布时间|
|price|是|float|价格|
|ext_info|否|array|额外信息|
|cover_img|是|array|封面图|
|cstaff|是|string|操作者|
|lv5_category_id|否|string|五级分类ID|

**请求示例**

```json
{
  "product_type": "pg_class",
  "product_short_name": "考研课",
  "start_time": "2019-02-11 13:00:00",
  "price": 299.00,
  "cover_img": {
    "url": "http://static.thefair.net.cn/note/cover/20190409/022a52d37c6d36708566e3b916eda2f1.jpeg",
    "name": "022a52d37c6d36708566e3b916eda2f1",
    "img_info": {"scale":0.75,"width":600,"height":800,"type":"jpg","size":53531}
  },
  "cstaff": "lichangao"
}
```

**返回示例**

```json
{
  "code": "0",
  "message": "",
  "result": {
    "item_id": "3123948988382950569"
  }
}
```

 **返回参数说明** 

|参数名|类型|说明|
|:-----|:-----|-----|
|item_id|string|商品ID|

 **备注** 
 
- product_type 枚举说明
  - 考研课程：pg_class
  - 英语课程：english_class
  - 火箭单词：rocket_class
  - 元气读书：lemon_class
- 旧版接口
  - 创建英语课程：`/backend/productadmin/add_english_class_item`
  - 创建考研课程：`/backend/productadmin/add_pg_class_item`
  - 创建火箭单词课程：`/backend/productadmin/create_rocket_class_item`
  - 创建元气读书商品：`/backend/productadmin/create_lemon_class_item`
- 思维导图
![](/assets/创建商品.png)