# Surviving Mars Thai Translations
### สำหรับผู้เล่นที่ต้องการร่วมทดสอบ
1. กดสมัครสมาชิกบนสตีมเวิร์กชอปที่ http://steamcommunity.com/sharedfiles/filedetails/?id=1335965052
2. อ่านวิธีการดาวน์โหลดและติดตั้งไฟล์เพิ่มเติมที่ https://github.com/iAmMutun/SurvivingMarsTH/releases/

### การแปล
___โปรดทราบ__ ตั้งแต่วันที่ 8 เมษายน 2561 เป็นต้นไปทางทีมแปลของดการเปิดเผยคำแปลบน GitHub เพื่อป้องกันการคัดลอก กรุณาติดต่อทีมแปลปัจจุบันหากคุณต้องการเข้าร่วมทีมกับเรา ส่วนไฟล์อื่นๆจะยังคงมีการอัพเดทบน GitHub เป็นระยะๆต่อไป_

แปลภาษาได้ในไฟล์ [Game.csv](Game.csv) โปรดงดแก้ไขไฟล์ Game.csv ในโฟลเดอร์ Thai Translations

หากคุณใช้งาน Windows ให้เรียกใช้คำสั่ง `.\tuftmf_x64.exe .\Game.csv '.\Thai Translations\Game.csv'` หลังการแปลเพื่อรันโปรแกรมแก้ไขวรรณยุกต์ลอย ก่อนทำการโหลดม็อดเข้าเกม หรืออัพโหลดขึ้นเวิร์กชอป  อ่านเพิ่มเติมเกี่ยวกับ tuftmf [ข้างล่าง](#tuftmf) 

### วิธีสร้างไฟล์เพิ่มเติม
* เนื่องจากตัวเกมไม่มีฟอนต์ภาษาไทยในตัว จึงต้องทำการแก้ไขไฟล์ hpk เพื่อเพิ่มเติมฟอนต์ในเกม
* ดาวน์โหลดโปรแกรมจัดการไฟล์ hpk จาก https://github.com/nickelc/hpk/releases
* สร้างโฟลเดอร์เปล่าๆ `Packs/Fonts/`
* ค้นหาโฟลเดอร์ที่ติดตั้งเกม เช่น `C:/Program Files/Steam/steamapps/common/Surviving Mars`
* แตกไฟล์ด้วยคำสั่ง `hpk.exe extract '[IntallationDir]/Packs/Fonts.hpk' 'Packs/Fonts'` โดยที่ [IntallationDir] คือโฟลเดอร์ที่ติดตั้งเกม
* ดาวน์โหลดฟอนต์และนำไฟล์ .ttf ไปไว้ในโฟลเดอร์ `Packs/Fonts/` ฟอนต์ที่ใช้ ณ ปัจจุบันคือ
    * [Ekkamai Standard](http://www.f0nt.com/release/ekkamai-standard/)
    * [iannnnnGMO](http://www.f0nt.com/release/iannnnngmo/)
* รวมไฟล์ฟอนต์ด้วยคำสั่ง `hpk.exe create --compress Packs/Fonts/ Packs/Fonts.hpk`
* นำไฟล์ Fonts.hpk ไปแทนที่ไฟล์เก่าในโฟลเดอร์ที่ติดตั้งเกม (กรุณาสำรองไฟล์ Fonts.hpk เก่าก่อนแทนที่)
* สร้างไฟล์ HPK เปล่าๆสำหรับบอกเกมให้รองรับภาษาไทยด้วยคำสั่ง `hpk.exe create Local/Thai Local/Thai.hpk`
* นำไฟล์ Thai.hpk ไปเพิ่มไว้ในโฟลเดอร์ย่อย Local ของโฟลเดอร์ที่ติดตั้งเกม

### tuftmf
โปรแกรมแก้วรรณยุกต์ลอย Thai Unicode Floating Tone Marks Fixer (TUFTMF) การทำงานคือรหัส Unicode วรรณยุกต์และสระบางตัวในสตริงจะถูกแก้ไขให้เป็นรหัส Unicode ใน Private Use Areas ที่ฟอนต์ไทยใช้เก็บอักขระที่อยู่ในตำแหน่งที่ดีกว่า ทำให้ผลลัพธ์การแสดงผลภาษาไทยออกมาสวยงามขึ้น โปรแกรมนี้ทำงานได้ผลกับเฉพาะฟอนต์บางตัวเท่านั้น 
โปรเจ็คต์บน GitHub: https://github.com/iAmMutun/tuftmf
