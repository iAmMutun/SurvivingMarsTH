# Surviving Mars Thai Translations
### สำหรับผู้เล่นที่ต้องการร่วมทดสอบ
1. กดสมัครสมาชิกบนสตีมเวิร์กชอปที่ http://steamcommunity.com/sharedfiles/filedetails/?id=1335965052
2. อ่านวิธีการดาวน์โหลดและติดตั้งไฟล์เพิ่มเติมที่ https://github.com/iAmMutun/SurvivingMarsTH/releases/tag/dep1

### แปลไทย
ร่วมแปลภาษาไทยได้ในไฟล์ [Thai Translations/Game.csv](Thai%20Translations/Game.csv)

### วิธีสร้างไฟล์เพิ่มเติม
* เนื่องจากตัวเกมไม่มีฟอนต์ภาษาไทยในตัว จึงต้องทำการแก้ไขไฟล์ Fonts.hpk เพื่อเพิ่มเติมฟอนต์ในเกม
* ดาวน์โหลดโปรแกรมจัดการไฟล์ HPK จาก https://github.com/nickelc/hpk/releases
* แตกไฟล์ `hpk.exe extract <IntallationDir>/Packs/Fonts.hpk Packs/Fonts` โดยที่ <IntallationDir> คือโฟลเดอร์ที่ติดตั้งเกม เช่น `C:/Program Files/Steam/steamapps/common/Surviving Mars`
* ดาวน์โหลดฟอนต์และนำไฟล์ .ttf ไปไว้ในโฟลเดอร์ [Packs/Fonts/](Packs/Fonts/)
    * [Ekkamai Standard](http://www.f0nt.com/release/ekkamai-standard/)
    * [Thai Sans Lite](http://www.f0nt.com/release/thai-sans-lite/)
* รวมไฟล์ฟอนต์ `hpk.exe create --compress Packs/Fonts/ Fonts.hpk`
* สร้างไฟล์ HPK เปล่าๆสำหรับบอกเกมให้รองรับภาษาไทย `hpk.exe create Local/Thai Local/Thai.hpk`
