# newUser
新增使用者帳戶資料

### HTTP Request
```
http://192.168.11.80:3030/johnnyHire/api/v1/newUser
```
### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:-----|:-----|
| cpy_id | 97090920 | String | 公司代號 | Y | n/a |
| cpy_name | 英特內軟體 | String | 公司名稱，會使用此名稱作為chat bot名稱，所以僅需要名稱即可。(ex.英特內軟體股份有限公司，僅需要「英特內軟體」即可。) | Y | n/a |
| email | inter@interinfo.com.tw | String | 公司Email | Y | n/a |
| password | 12345 | String | 登入密碼 | Y | n/a |
| token | API-Token | String | 識別使用API權限 | Y | n/a |

### JSON representation
```json
{
  "cpy_id": "97090920",
  "cpy_name": "英特內軟體",
  "email": "inter@interinfo.com.tw",
  "password": "12345",
  "token": "API-Token"
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| cpy_id | String | 使用公司統編 |
| cpy_name | String | Chat Bot小助手名稱 |
| email | String | 作為登入帳號 |
| password | String | 加密後再寫入資料庫 |
| token | String | 需要使用此API時，會提供相對應token |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "使用者資料設定成功!!"
    ],
    "data": {
        "CPY_ID": "97090920",
        "CPY_NAME": "英特內軟體",
        "EMAIL": "inter@interinfo.com.tw",
        "PASSWORD": "$2a$10$rc6b9bL4JViQI.1lk5jZneQ0ANB2GdckqI41vI29nreYX693w620S",
        "INDUSTRY_NO": "97090920",
        "ISADMIN": false,
        "ISHR": false,
        "WHICH_ROLE": "hire"
    }
}
```

### HTTP Response when Failed
```json
{
    "status": "fail",
    "code": 400,
    "message": [
        "XXX"
    ],
    "data": {}
}
```

### HTTP Response when Exception
```json
{
    "status": "fail",
    "code": 409,
    "message": [
        "XXX"
    ],
    "data": {}
}
```

