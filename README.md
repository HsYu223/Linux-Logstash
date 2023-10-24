# Linux-Logstash

Linux Logstash Iinstall and run as services

--下載rpm

-- https://www.elastic.co/downloads/past-releases/logstash-8-10-2

sudo rpm -vi logstash-8.10.2-x86_64.rpm

-- 移至執行目錄

cd /usr/share/logstash

-- 建立config目錄, 放入對應設定檔

mkdir config

-- 安裝離線套件

./bin/logstash-plugin install file://{離線套件.zip檔案路徑}

-- 產生 /etc/systemd/system/logstash.service

./bin/system-install

-- 開機啟動

sudo systemctl enable logstash.service

-- 設定重新載入

systemctl daemon-reload

-- 啟動

sudo systemctl start logstash.service

