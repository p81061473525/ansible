練習題目 : 
1. 請於 root 目錄 創建 ansible 工作 資料夾，
   1. 環境設定以下項目
   -  可以控制被控端主機。
   -  主機清單必須在工作目錄底下。   
3. 請撰寫 machine.yaml 主機資訊蒐集劇本，
   1. 蒐集以下資訊，並將資訊蒐集至主控端 ~ 目錄底下 :
   - 主機名稱
   - 主機作業系統
   - 主機作業系統家族
   - 主機系統架構
   - 主機IP位置
   - 主機硬碟資訊
   - 主機記憶體大小
4. 請撰寫 update.yaml 全機軟體 更新劇本，內容包括，
   1. 更新 YUM 所有套件
   2. 安裝 netstat 
   - 確認 netstat 軟件
   - 安裝 netstat 軟件
   - 確認 netstat 安裝
   3. 更新 repo 並安裝 htop 
   - 移除 htop 軟件。
   - 確認 htop 移除。
   - 移除 YUM epel-release ，
   - 使用 內建模組新增 "epel 昌庫"，
   - 安裝 htop 軟件。
   - 確認 htop 安裝。
5. 請撰寫 install_nginx.yaml nginx 建置劇本，
   1. 並使每個主機訪問 80 port 正常訪問
   2. 將 template/index.html 複製到 nginx 預設目錄，讓訪問 port 可以 顯示 Hello World。
   3. 請使用 uri 模組驗證 hello world。
   4. 請使用 shell 模組驗證 hello world。
   5. 將 template/apple.conf 複製到 nginx conf 目錄，讓訪問 57222 port 可以顯示 APPLE hello world。
6. 請撰寫 facts.ymal 主控制端 以下項目
   1. 劇本請顯示以下項目 : 
   - 被控制端群組 所在群組
   - 主機設備清單 所有主機群組名稱與資料
   - 主機設備清單 所在位置
   - 本劇本所在位置 
7. 請創建 user.yaml 使用者劇本，
   1. 請使用 變數 與 變數名稱檔案 的方式，創建 關係圖如下人員
   - admin 群組成員 john,mary,ha 
   - user 群組成員 user1,user2,user3,user4
8. 請創建 loop-yum.yaml 迴圈劇本
   1. 使用迴圈 loop 方式，安裝
   - nginx 
   - httpd 
9. 請創建 iptables.yaml 防火牆劇本
   1. 請使用 template/iptable.sh 範本，僅讓 192.168.50.200 主控端訪問各自節點，而各自節點間無法訪問。
10. 承接 第5題 nginx 題目，
   1. 複製一份 template/apple.conf 改成 template/SAMPLE.conf，並將相關變數替換。
   - 57222 替換成為 SAMPLE_LISTEN_PORT
   - apple.com 替換成為 SAMPLE_SERVER_NAME
   - root 位置請替換成為 SAMPLE_ROOT_PATH
   2. 請撰寫 nginxsample.yaml 劇本，並使用相關變數，建立兩個網站，內容必須顯示相關域名。
12. 請創建 條件劇本 
13. 請創建 LVM.yaml，完成一次 LVM 切割操作。
14. 請將 inventory 進行加密，解密，重製密碼，最後訪問 inventory 內容必須要可以須入密碼才能訪問主機資訊。
# 15. playbook CICD

