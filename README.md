# 安裝與執行指引

## 1.下載專案
clone專案並導至專案位置
```bash
git clone https://github.com/DanielTseng2004/studentHub.git
cd yourpath/studentHub
```
## 2.安裝及執行前端
進到前端目錄後，安裝所需套件
```bash
cd front
npm i
```

執行前端
```bash
npm run dev
```

## 3.安裝及執行後端
進到後端目錄後，安裝所需套件
```bash
cd backDB
npm i
```

將 .env.example 文件重命名為 .env並修改為你的設定

```env
DBUSER = user             # 資料庫使用者
DBPASSWORD=password       # 資料庫密碼
DBHOST=127.0.0.1          # 資料庫連線位置
DBPORT=DBport             # 資料庫連線埠
DBNAME=name               # 資料庫名稱
PORT=8888                 # 後端監聽位置
LogPath=logs              
assetsPath=/assets        
HomePagePath=/index.html  
privateKey=key            
```

執行後端伺服器
```bash
npm run dev
```

## 4.資料庫連接
先安裝MongoDB並啟動，建立`students` collection 並匯入範例數據`studentslist.csv`

範例格式如下:
```json
{
    "userName":"tkume2253",
    "sid":4,
    "name":"***",
    "department":"機械工程系",
    "grade":"四年級",
    "class":"B",
    "email":"tkume2253@tkuim.com"
}
```

# API 規格說明
## 1.查詢所有學生資料
+ **請求**
    + `GET /api/v1/user/findAll`
+ **回應**
    + ```json 
        {
            "code": 200,
            "message": "find sucess",
            "body":
                {
                    "_id": "67592089d431b1143e5bc7fb",
                    "userName": "tkume2253",
                    "sid": "4",
                    "name": "好難喔",
                    "department": "機械工程系",
                    "grade": "四年級",
                    "class": "B",
                    "email": "tkume2253@tkuim.com"
                },"...共N筆資料
        }
        
        ```

## 2.根據 ID 查詢學生資料
+ **請求**
    + `GET /api/v1/user/findAll` 
+ **回應**
    + ```json 
        {
            "code": 200,
            "message": "find sucess",
            "body":
                {
                    "_id": "67592089d431b1143e5bc7fb",
                    "userName": "tkume2253",
                    "sid": "4",
                    "name": "好難喔",
                    "department": "機械工程系",
                    "grade": "四年級",
                    "class": "B",
                    "email": "tkume2253@tkuim.com"
                },
        }

        ```
## 3.新增學生資料
## 4.根據 ID 刪除學生資料
## 5.根據 ID 更新學生資料