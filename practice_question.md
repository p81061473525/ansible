練習題目 : 
1. 請於 root 目錄 創建 ansible 工作 資料夾，
   1. 環境設定以下項目
   -  可以控制被控端主機。
   -  主機清單必須在工作目錄底下。   
2. 請撰寫 machine.yaml 主機資訊蒐集劇本，
   1. 請將 Selinux 關閉
   2. 請重啟主機三次，並且每次重啟需要告知 ”第幾次重啟“
   3. 蒐集以下資訊，並將資訊蒐集至主控端 ~ 目錄底下 :
   - 主機名稱
   - 主機作業系統
   - 主機作業系統家族
   - 主機系統架構
   - 主機IP位置
   - 主機硬碟資訊
   - 主機記憶體大小
3. 請撰寫 update.yaml 全機軟體 更新劇本，內容包括，
   1. 更新 YUM 所有套件
   2. 安裝 netstat 
   3. 更新 repo 並安裝 htop 
   - 移除 htop 軟件。
   - 確認 htop 移除。
   - 移除 YUM epel-release ，
   - 使用 內建模組新增 "epel 昌庫", repo設定檔案 名稱為 epelansible.repo
   - 安裝 htop 軟件。
   - 確認 htop 安裝。
4. 請撰寫 install_nginx.yaml nginx 建置劇本，
   1. 並使每個主機訪問 80 port 正常訪問
   2. 將 template/index.html 複製到 nginx 預設目錄，讓訪問 port 可以 顯示 Hello World。
   3. 請使用 uri 模組驗證 hello world。
   4. 請使用 shell 模組驗證 hello world。
   6. 被控制端創建 /usr/share/nginx/html/apple
   7. 將 template/apple.conf 複製至被控制端主機 /usr/share/nginx/html/apple ，並使 56672 可以正常被訪問。
   8. 使用 變數檔案 方式設計 sample.conf，並將 sample.conf 複製到被控制端主機後，能訪問以下符合需求的項目
   - banana.conf , server_name _ , port 56673 , 內容為 主機名稱 : banana.com , ex: as-50-200 : banana.com
   - cat.com , server_name _ , port 56674 , 內容為 主機名稱 : cat.com , ex: ac-50-201 : cat.com
   - dog.com , server_name _ , port 56675 , 內容為 主機名稱 : dog.com , ex: ac-50-202 : dog.com
5. 請撰寫 facts.ymal 主控制端 以下項目
   1. 劇本請顯示以下項目 : 
   - 被控制端群組 所在群組
   - 主機設備清單 所有主機群組名稱與資料
   - 主機設備清單 所在位置
   - 本劇本所在位置 
6. 請創建 user.yaml 使用者劇本，
   1. 請使用 變數 與 變數名稱檔案 的方式，創建 關係圖如下人員
   - admin 群組成員 john,mary,ha 
   - user 群組成員 user1,user2,user3,user4  
7. 請創建 loop-yum.yaml 迴圈劇本  
   1. 使用迴圈 loop 方式，安裝  
   - nginx  
   - httpd
8. 請創建 iptables.yaml 防火牆劇本
   1. 請使用 template/iptable.sh 範本，僅讓 192.168.50.200 主控端訪問各自節點，而各自節點間無法訪問  
10. 請創建 條件劇本 
11. 請創建 LVM.yaml，完成一次 LVM 切割操作。
12. 請將 inventory 進行加密，解密，重製密碼，最後訪問 inventory 內容必須要可以須入密碼才能訪問主機資訊。
# 15. playbook CICD

