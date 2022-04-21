# Docker MySQL

## Docker Run Command
    docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD="123456" -e TZ=Asia/Hong_Kong -d mysql:8.0.22

---
## Variables
### lower-case-table-names

    說明是否資料目錄所在的檔案系統對檔名的大小寫敏感

| Value | Meaning |
| :---: | --- |
| 0 | 大小寫敏感 |
| 1 | 大小寫不敏感。建立的表，資料庫都是以小寫形式存放在磁碟上，對於sql語句都是轉換為小寫對錶和DB進行查詢 |
| 2 | 建立的表和DB依據語句上格式存放，凡是查詢都是轉換為小寫進行 |

    docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD="123456" -e TZ=Asia/Hong_Kong -d mysql:8.0.22 --lower-case-table-names=1