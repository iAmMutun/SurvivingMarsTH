# Surviving Mars Thai Translations
### สำหรับผู้เล่นที่ต้องการร่วมทดสอบ
1. กดสมัครสมาชิกบนสตีมเวิร์กชอปที่ http://steamcommunity.com/sharedfiles/filedetails/?id=1335965052
2. ดาวน์โหลดและติดตั้งไฟล์เพิ่มเติมที่ https://github.com/iAmMutun/SurvivingMarsTH/releases/tag/dep1

### แปลไทย
ร่วมแปลภาษาไทยได้ในไฟล์ [Thai Translations/Game.csv](Thai%20Translations/Game.csv)

### วิธีสร้างไฟล์เพิ่มเติม
* เนื่องจากตัวเกมไม่มีฟอนต์ภาษาไทยในตัว จึงต้องทำการแก้ไขไฟล์ Fonts.hpk เพื่อเพิ่มเติมฟอนต์ในเกม
* ดาวน์โหลดโปรแกรมจัดการไฟล์ HPK จาก https://github.com/nickelc/hpk/releases
* คัดลอกไฟล์ Fonts.hpk จากโฟลเดอร์เกม (C:/Program Files/Steam/steamapps/common/Surviving Mars/Packs) มาไว้ใน [Packs/](Packs/)
* แตกไฟล์ `hpk.exe extract Packs/Fonts.hpk Packs/Fonts`
* ดาวน์โหลดฟอนต์และนำไฟล์ .ttf ไปไว้ในโฟลเดอร์ [Packs/Fonts/](Packs/Fonts/)
    * [Ekkamai Standard](http://www.f0nt.com/release/ekkamai-standard/)
    * [Thai Sans Lite](http://www.f0nt.com/release/thai-sans-lite/)
* รวมไฟล์ `hpk.exe create --compress Packs/Fonts/ Fonts.hpk`
