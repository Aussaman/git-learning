# 5-Day Git & GitHub Learning Challenge

> โครงการเรียนรู้ทักษะใหม่ด้วยตนเองภายใน 5 วัน ร่วมกับการถ่ายทอดความรู้ด้วย Feynman Technique  
> จัดทำขึ้นเพื่อบันทึกการเรียนรู้และการฝึกปฏิบัติการใช้งาน Git และ GitHub ตั้งแต่ระดับพื้นฐานจนถึงการทำงานร่วมกันบน Cloud

---

## ข้อมูลผู้จัดทำ
* **ชื่อ-นามสกุล:** Aussaman Sriwichai
* **อีเมล:** aussamans68@nu.ac.th
* **ทักษะที่เลือกเรียนรู้:** Git & GitHub Version Control System
* **ระดับความรู้ก่อนเริ่ม:** เคยลองศึกษาเบื้องต้นแต่ยังไม่เข้าใจแก่นการทำงาน (ระดับ 3-4)

---

## วัตถุประสงค์ของโปรเจกต์ (Objectives)
1. เข้าใจโครงสร้างและกลไกการทำงานของ Git (Working Directory -> Staging Area -> Local Repository -> Remote Repository)
2. ฝึกฝนคำสั่งพื้นฐานในการควบคุมเวอร์ชันของซอร์สโค้ดในเครื่องตนเอง
3. สามารถบริหารจัดการกิ่งงาน (Branching) และรวมงานกลับเข้าสู่สายหลัก (Merging) ได้อย่างถูกต้อง
4. จำลองข้อผิดพลาดที่พบบ่อยในการทำงานจริง และฝึกแก้ไขปัญหาด้วยตนเอง เช่น Merge Conflict, Push Rejected
5. สามารถทำงานร่วมกับระบบ Cloud อย่าง GitHub ผ่านการ Push/Pull และสร้าง Pull Request (PR)
6. สามารถอธิบายแก่นของ Git ให้ผู้อื่นเข้าใจได้ง่ายตามหลักการ Feynman Technique

---

## โครงสร้างไฟล์ใน Repository (Project Structure)

| ชื่อไฟล์ | บทบาทและรายละเอียด |
| :--- | :--- |
| [`README.md`](README.md) | เอกสารสรุปภาพรวมโปรเจกต์ วัตถุประสงค์ ขั้นตอนการดำเนินงาน และคำสั่งทั้งหมด |
| [`hello.py`](hello.py) | สคริปต์แรกในการฝึกฝนคำสั่ง `git init`, `git add` และการบันทึก `git commit` ครั้งแรก |
| [`login.py`](login.py) | ฟีเจอร์ที่พัฒนาแยกออกมาใน Branch `feature-login` เพื่อทดสอบการแตกกิ่งและการ Merge |
| [`goodbye.py`](goodbye.py) | สคริปต์ที่พัฒนาขึ้นใน Branch `feature-goodbye` เพื่อทดสอบการส่ง Pull Request บน GitHub |

---

## บันทึกการเรียนรู้รายวัน (5-Day Learning Journey)

### Day 1: วางแผนและทำข้อตกลงการเรียนรู้ (Learning Contract)
* กำหนดหัวข้อการเรียนรู้: Git & GitHub
* ศึกษาภาพรวมว่า Version Control คืออะไร และความสำคัญในการพัฒนาซอฟต์แวร์
* กำหนดเกณฑ์วัดผลสำเร็จ: สามารถสร้าง Local Repo, Push ขึ้น Cloud, จัดการ Branch, แก้ไข Conflict และอธิบายให้ผู้อื่นเข้าใจได้

### Day 2: ติดตั้งและบันทึกประวัติการทำงานแรก
* ติดตั้งโปรแกรม Git for Windows (v2.55.0)
* ตั้งค่าข้อมูลผู้ใช้งานระดับ Global (`user.name` และ `user.email`)
* เริ่มต้นสร้าง Repository ด้วย `git init` ในโฟลเดอร์ `git-learning`
* ฝึกฝนวงจรการ Commit พื้นฐาน: สร้างไฟล์ -> `git add .` -> `git commit -m "first commit: add README"`

### Day 3: การทำงานกับ Branch, Cloud และการจำลองข้อผิดพลาด
* เชื่อมโยง Local Repository กับ Remote Repository บน GitHub (`git remote add origin`)
* แตกกิ่งงานใหม่เพื่อพัฒนาฟีเจอร์อย่างปลอดภัยด้วย `git checkout -b feature-login`
* รวมโค้ดกลับเข้าสู่สายหลักด้วย `git merge feature-login` และอัปโหลดขึ้น GitHub ด้วย `git push`
* จำลองและแก้ไขข้อผิดพลาดสำคัญ 3 กรณี:
  1. Push Rejected (non-fast-forward) จากการที่ Remote มีการแก้ไขก่อน
  2. Merge Conflict จากการแก้ไขบรรทัดเดียวกันพร้อมกันในสองกิ่ง
  3. Pathspec Error จากการพิมพ์ชื่อ Branch ผิด
* สร้าง Pull Request (PR #2) บนหน้าเว็บ GitHub และทำการ Merge เข้า `main` สำเร็จ

### Day 4: ถ่ายทอดความรู้ด้วย Feynman Technique
* ถ่ายทอดเนื้อหาเรื่อง Git & GitHub ให้เข้าใจง่ายโดยใช้การเปรียบเทียบ (Analogy):
  * **Git = ระบบ Save Game:** ช่วยบันทึกจุด checkpoint ของโค้ด หากเกิดข้อผิดพลาดสามารถย้อนกลับมายังจุดบันทึกเดิมได้เสมอ
  * **Branch = ห้องทดลองแยก:** พัฒนาฟีเจอร์ใหม่ในพื้นที่แยก หากสำเร็จจึงรวมกลับเข้าห้องหลัก (main) หากล้มเหลวสามารถลบทิ้งได้โดยไม่กระทบงานหลัก
  * **Merge Conflict = การแก้ไขเอกสารทับซ้อน:** คล้ายกรณีที่สองคนแก้ไขข้อความในบรรทัดเดียวกัน Git จึงหยุดเพื่อให้ผู้ใช้ตัดสินใจเลือกเนื้อหาที่ถูกต้อง
* บันทึกวิดีโออธิบายความยาว 3-5 นาทีโดยไม่ผ่านการตัดต่อ

### Day 5: ตรวจสอบประวัติการทำงานและสะท้อนคิด (Reflection)
* เรียกดูประวัติการทำงานทั้งหมดในรูปแบบโครงสร้างต้นไม้ด้วยคำสั่ง `git log --oneline --graph --all`
* ทบทวนสิ่งที่ได้เรียนรู้และสรุปบทสะท้อนคิด (Reflection) ครบทั้ง 6 ข้อ

---

## สรุปคำสั่ง Git สำคัญที่ได้ฝึกปฏิบัติ (Cheat Sheet)

### 1. การเริ่มต้นและตั้งค่า (Setup & Config)
```bash
# ตรวจสอบเวอร์ชันของ Git
git --version

# กำหนดชื่อและอีเมลสำหรับระบุตัวตนของผู้บันทึก
git config --global user.name "Aussaman Sriwichai"
git config --global user.email "aussamans68@nu.ac.th"

# เริ่มต้นสร้าง Git Repository ในโฟลเดอร์ปัจจุบัน
git init
```

### 2. วงจรการทำงานพื้นฐาน (Basic Workflow)
```bash
# ตรวจสอบสถานะของไฟล์ใน Working Directory และ Staging Area
git status

# นำไฟล์เข้าสู่ Staging Area เพื่อเตรียมพร้อมสำหรับการบันทึก
git add .
git add <filename>

# บันทึกสถานะของโปรเจกต์พร้อมข้อความกำกับ
git commit -m "commit message"

# เรียกดูประวัติการบันทึกทั้งหมด
git log --oneline
git log --oneline --graph --all
```

### 3. การจัดการกิ่งงาน (Branch & Merge)
```bash
# ดูรายชื่อ Branch ทั้งหมดที่มีอยู่ในระบบ
git branch

# สร้าง Branch ใหม่และสลับไปทำงานที่ Branch นั้นทันที
git checkout -b <branch-name>

# สลับไปยัง Branch ที่ต้องการ
git checkout <branch-name>

# รวมกิ่งงานย่อยกลับเข้าสู่กิ่งหลัก (ต้องอยู่ที่กิ่งหลักก่อนรันคำสั่ง)
git merge <branch-name>

# ลบ Branch ที่ใช้งานเสร็จแล้ว
git branch -d <branch-name>
```

### 4. การทำงานร่วมกับระบบ Cloud (Remote & Collaboration)
```bash
# ผูก Local Repository เข้ากับ GitHub Repository
git remote add origin https://github.com/Aussaman/git-learning.git

# ส่งโค้ดจากเครื่องขึ้นไปยัง GitHub
git push -u origin main
git push

# ดึงโค้ดเวอร์ชันล่าสุดจาก GitHub ลงมาที่เครื่อง
git pull
```

---

## บันทึกข้อผิดพลาดที่พบและการแก้ไข (Troubleshooting)

### กรณีที่ 1: `! [rejected] (non-fast-forward)`
* **สาเหตุ:** มีการเปลี่ยนแปลงไฟล์บน GitHub แต่ในเครื่องเรายังไม่มีข้อมูลล่าสุด ทำให้ Git ปฏิเสธการ Push
* **วิธีแก้ไข:** ดึงข้อมูลล่าสุดลงมาผสานที่เครื่องก่อนด้วยคำสั่ง `git pull` แล้วจึงสั่ง `git push` อีกครั้ง

### กรณีที่ 2: `CONFLICT (content): Merge conflict in ...`
* **สาเหตุ:** มีการแก้ไขไฟล์เดียวกันในบรรทัดเดียวกันจากสอง Branch ทำให้ Git ไม่สามารถตัดสินใจรวมไฟล์ได้โดยอัตโนมัติ
* **วิธีแก้ไข:** 
  1. เปิดไฟล์ที่มีปัญหาขึ้นมาดู จะพบเครื่องหมาย `<<<<<<< HEAD`, `=======` และ `>>>>>>>`
  2. ลบเครื่องหมายของ Git ออก และแก้ไขข้อความให้เหลือเฉพาะเวอร์ชันที่ถูกต้อง
  3. สั่ง `git add .` และทำการบันทึกด้วย `git commit -m "resolve conflict"`

### กรณีที่ 3: `error: pathspec '<name>' did not match any file(s)`
* **สาเหตุ:** พิมพ์ชื่อ Branch ที่ต้องการสลับไปผิด หรือ Branch นั้นยังไม่ได้ถูกสร้างขึ้น
* **วิธีแก้ไข:** ใช้คำสั่ง `git branch` เพื่อตรวจดูรายชื่อ Branch ทั้งหมดก่อน แล้วจึงพิมพ์คำสั่งสลับชื่อให้ถูกต้อง

---

## สิ่งที่ได้รับจากกิจกรรม (Key Takeaways)
* การใช้ Version Control ช่วยลดความกังวลในการเขียนโปรแกรม เนื่องจากสามารถตรวจสอบและย้อนกลับไปยังเวอร์ชันที่ทำงานได้เสมอ
* การใช้งาน Branch ช่วยให้การพัฒนาฟีเจอร์ใหม่ทำได้อย่างอิสระและปลอดภัย ไม่ส่งผลกระทบต่อเสถียรภาพของโค้ดหลัก
* การอธิบายเนื้อหาทางเทคนิคให้ผู้อื่นเข้าใจได้ง่ายโดยใช้ภาษาทั่วไป (Feynman Technique) เป็นเครื่องมือวัดระดับความเข้าใจของตนเองได้อย่างชัดเจน

---
*จัดทำขึ้นสำหรับการส่งงาน 5-Day Learning Challenge*  
*Repository Link: [https://github.com/Aussaman/git-learning](https://github.com/Aussaman/git-learning)*
