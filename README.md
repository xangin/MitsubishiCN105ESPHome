# MitsubishiCN105ESPHome (Simon’s Customized Version for ESP32-C3)

This is a customized version of [echavet/MitsubishiCN105ESPHome](https://github.com/echavet/MitsubishiCN105ESPHome).  
It includes ESPHome YAML configurations targeting the ESP32-C3 platform, along with usage notes for integrating Mitsubishi HVAC systems via CN105.

適用廠牌: **三菱電機冷氣**，壁掛、吊隱皆可

**適用型號: 需拆開機殼找出機板上有個暗紅色寫著CN105接頭，有這個就能控制**

基本上只要修改最頂端的兩個名稱即可，方便OTA與辨識是哪一台

`climate-mt.factory.bin`適用USB線直接燒錄，想自行修改YAML請參考`ESP32C3-example.yaml`

`climate-mt.ota.bin`僅供燒錄過OTA更新用

## 如何下載

點擊檔案名稱>點右上角有個下載的圖案(Download Raw file)>儲存

## 使用方法

### A. 透過USB

1. 模組透過usb接上電腦
2. 用chrome或edge瀏覽器前往 [https://web.esphome.io](https://web.esphome.io/)
3. 按Connect>選擇寫USB JTAG(小)>按INSTALL>選擇剛儲存的Bin檔，等待燒錄完成
4. 顯示finish後，就可看到ESP32上面的藍燈開始閃爍，這時候等待久一點，會看到有熱點跑出來
5. 點連線並輸入Wi-Fi密碼: 12345678
6. 連上後輸入http://192.168.4.1
7. 進到網頁選擇家中Wi-Fi名稱及輸入密碼後按儲存，連上後HA應該就會自動發現此裝置

### B. OTA

1. 在瀏覽器網址列輸入裝置IP
2. 最下方OTA Update選擇ota.bin檔>按Update，等待畫面跳轉為done即完成



## 📦 Credits
This project is based on the excellent work of [echavet/MitsubishiCN105ESPHome](https://github.com/echavet/MitsubishiCN105ESPHome), which itself integrates multiple community contributions.  
Licensed under MIT.
