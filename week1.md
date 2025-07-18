# UPDATE WEEK 1
**Work Done**
- จากการ label ที่ได้จากพี่พัด > จัดกลุ่ม knowledge base และ คำถาม testcase ได้ออกเป็น 3 กลุ่มใหญ่(category_level1)คือ หัตถการ, อาการภาวะแทรกซ้อน, การปฏิบัติตัวหลังการทำหัตถการ และสามารถแบ่งข้อมูลเป็นกลุ่มย่อย(category_level2) ได้ดังนี้
https://docs.google.com/spreadsheets/d/1zRpd1Q497p9hYsMoIfLdI0lq1hZaRCyf5bI6PKRuFgs/edit?gid=0#gid=0
<img width="1055" height="1171" alt="image" src="https://github.com/user-attachments/assets/f6b218a5-daa1-42f5-be06-7bca8cf8823b" />

- เพิ่ม testcase ประมาณ100 ข้อ > รอการตรวจสอบจากพี่พัด
https://docs.google.com/spreadsheets/d/1lTouFnO2R0IztEecpepUd7B1QMfLsr5f/edit?gid=214918395#gid=214918395
  
**Future Work**
- (อาจจะต้องแก้ส่วนของการแบ่ง category)
เนื่องจาก criteria ใน prompt จะเป็น true ได้ require ให้มี > คำถาม + หัตถการ + บริบท > เลยต้องแก้การแบ่งกลุ่มเป็น category1 คือหัตถการ, category2 คือบริบท(เช่น food,bleeding, pain, workout)
- ดูเรื่อง benchmark
- draft benchmark
  - category_level1 -> หัตถการ: หัตถการทั้งหมด เช่น extraction, third molar surgery, surgical removal of impacted teeth, surgical removal of impacted tooth, bone grafting, dental implant surgery
  - category_level2 -> บริบท: อาการภาวะแทรกซ้อน + การปฏิบัติตัวหลังการทำหัตถการ เช่น food, bleeding, pain, oral hygiene
  - ex. คำถาม: "หลังถอนฟันเลือดออกเยอะต้องทำยังไง" -> หัตถการ: extraction , บริบท: bleeding
  - Benchmark: วัด Accuracy ว่า AI ดึงข้อมูลจากไฟล์ที่มีlabelหัตถการและบริบทที่ตรงกัน (เช่น ไฟล์ที่มี "extraction" และ "bleeding")
