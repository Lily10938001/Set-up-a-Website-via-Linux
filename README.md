# Set-up-a-Website-via-Linux
Practicing for using Linux.

To be up on Linux, I randomly chose a html template online and set up a website via Linux.
Source :  https://www.free-css.com/free-css-templates

------------------------------------
VirtualBox setting : 
1.	CPU : 3顆
2.	記憶體 : 2000MB 
3.	光碟機 : CentOS 7.9.2009

CentOS : 
1.	localhost login : root
2.	打 ”nmcli” 得到inet4 : IP位址
3.	叫出cmd
4.	輸入”ssh root@IP位址” → “yes” → 輸入password → 即可從本機連線至CentOS的root使用者

架站 : 
1.	安裝 HTTP Server : yum install httpd
2.	啟動 HTTP Server : systemctl start httpd
3.	關閉Linux防火牆 : systemctl stop firewalld
4.	cd到想存放下載檔案的位置 : cd /var/www/html/
5.	直接遠端下載檔案 : yum install wget → wget 下載連結網址
6.	ls找到檔名並解壓縮 : yum install unzip → unzip 檔名
7.	暫時關閉Linux安全管理模式 : setenforce 0
8.	在瀏覽器上查詢 ”IP位址/解壓縮資料夾名稱” 就能成功看到網頁

編輯網頁HTML : 
1.	yum install vim → vim 下載檔html檔名(會直接開啟編輯頁面)
2.	查找內容(EX: title, image...) : “/內容” (用”n”找下一個)
3.	編輯 : ”I” → 改為自己的內容
