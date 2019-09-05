
# 快速开始

### 账号申请

 账号添加联系人： 古科明、刘媛媛
 
 打开RethinkDB，在Data Explorer执行
 ```
 r.db('stf').table('users').insert(
  [
    {
      "group": "FOPnIQ0mRJuwda/mi02kUg==" ,
      "email": "gukeming@ds.cn",
      "name": "古科明",
      "password": "123456",
    }
  ]
)
```
 
### 新增stf机器
  1. 把手机usb连接上stf
  2. 手机设置为开发者调试模式
  3. 同意stf调试该手机
  4. stf就会在列表中显示该手机
