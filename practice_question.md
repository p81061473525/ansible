練習題目 : 

- 隱藏題目 , 請設定 apple.conf , 網域 apple.com , 聽 57222 port，內容要顯示以下內容
- 隱藏題目 , 請設定 變數檔檔案 , 並使用 loop , 網路 XXX.com , 聽 不同的 port 號

1. 請撰寫 machine.yaml 主機資訊蒐集劇本，
   1. 蒐集以下資訊，並將資訊蒐集至主控端 ~ 目錄底下 :
   - 主機名稱
   - 主機作業系統
   - 主機作業系統家族
   - 主機系統架構
   - 主機IP位置
   - 主機硬碟資訊
   - 主機記憶體大小
2. 請撰寫 update.yaml 全機軟體 更新劇本，內容包括，
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
3. 請撰寫 install_nginx.yaml nginx 建置劇本，
   並使每個主機訪問 80 port 可以 顯示 hello world，
   驗證過程請使用 uri 模組，
   最後步驟請移除 nginx 並驗證。
   hint: 可以串建模板 index.html 
4. 請撰寫 facts.ymal 主控制端 以下項目
   - 被控制端群組 所在群組
   - 主機設備清單 所有主機群組名稱與資料
   - 主機設備清單 所在位置
   - 本劇本所在位置 
5. 請創建 user.yaml 
   - 包含 使用者群組 admin,user, 
     admin 群組成員 john,mary,ha 
     user 群組成員 user1,user2,user3,user4
# 7. 條件 劇本
# 8. 創建 防火牆劇本，只能夠允許 192.168.50.202 主機進入。
# 11. playbook CICD

