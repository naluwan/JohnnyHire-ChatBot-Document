# newPosition
新增職缺資訊

### HTTP Request
```
http://192.168.11.80:3030/johnnyHire/api/v2/newPosition
```
### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:-----|:-----|
| cpy_id | 97090920 | String | 公司代號 | Y | n/a |
| position_name | [研發處]研發工程師 | String | 職缺名稱 | Y | n/a |
| entity_name | rd | String | 職缺英文名稱 | Y | n/a |
| position_des | 【研發處】研發工程師薪資：<br>1.依據職位決定薪資福利及獎金制度。<br>2.採底薪+津貼+加給+獎金制。<br>3.月薪xx,xxx元 ~ xx,xxx元<br><br>【研發處】研發工程師工作內容：<br>1.機房、網路維運、硬體設備維護和相關軟硬體設備問題解決。<br>2.公司內部資訊系統、伺服器之儲存、備份規劃、管理。<br>3.使用者帳號與權限申請管控與開放、關閉。<br>4.環境管制區管控、整備。<br>5.設備維修、採購、保養、資產盤點。<br>6.資訊安全管理、稽核、風險管理。<br>7.主管交辦事項。<br>8.客戶端雲端服務主機維運。<br> | String | 職缺內容 | Y | n/a |
| token | API-Token | String | 識別使用API權限 | Y | n/a |

### JSON representation
```json
{
  "cpy_id": "97090920",
  "position_name": "【研發處】研發工程師",
  "entity_name": "rd",
  "position_des": "【研發處】研發工程師薪資：
  1.依據職位決定薪資福利及獎金制度。
  2.採底薪+津貼+加給+獎金制。
  3.月薪xx,xxx元 ~ xx,xxx元
  
  【研發處】研發工程師工作內容：
  1.機房、網路維運、硬體設備維護和相關軟硬體設備問題解決。
  2.公司內部資訊系統、伺服器之儲存、備份規劃、管理。
  3.使用者帳號與權限申請管控與開放、關閉。
  4.環境管制區管控、整備。
  5.設備維修、採購、保養、資產盤點。
  6.資訊安全管理、稽核、風險管理。
  7.主管交辦事項。
  8.客戶端雲端服務主機維運。",
  "token": "johnnyHire_API_Secret"
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| cpy_id | String | 使用公司統編 |
| position_name | String | 職缺中文名稱 |
| entity_name | String | 職缺英文名稱，讓機器人辨識用 |
| position_des | String | 機器人辨識出職缺後，給予相對應的回覆內容 |
| token | String | 需要使用此API時，會提供相對應token |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "新增職缺成功!!"
    ],
    "data": {
        "CPY_ID": "97090920",
        "CPY_NAME": "英特內軟體",
        "POSITION_ID": 1,
        "POSITION_NAME": "【研發處】研發工程師",
        "POSITION_DES": "【研發處】研發工程師薪資：\n1.依據職位決定薪資福利及獎金制度。\n2.採底薪+津貼+加給+獎金制。\n3.月薪xx,xxx元 ~ xx,xxx元\n\n【研發處】研發工程師工作內容：\n1.機房、網路維運、硬體設備維護和相關軟硬體設備問題解決。\n2.公司內部資訊系統、伺服器之儲存、備份規劃、管理。\n3.使用者帳號與權限申請管控與開放、關閉。\n4.環境管制區管控、整備。\n5.設備維修、採購、保養、資產盤點。\n6.資訊安全管理、稽核、風險管理。\n7.主管交辦事項。\n8.客戶端雲端服務主機維運。"
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

