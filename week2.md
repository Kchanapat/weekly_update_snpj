# UPDATE WEEK 2
**Work Done**
- file knowledge base: แก้ให้สามารถ label ให้มีหลาย actegory ได้
- file question: label เพิ่มว่าอันไหนใช้ ai generated หรือ คิดเอง
- Benchmark สำหรับประเมิน RAG ในการดึงข้อมูลจาก knowledge base ให้ตรงกับคำถาม
  - โดยกำหนดให้คำถามแต่ละข้อมีป้ายกำกับหมวดหมู่ที่ชัดเจนในสองระดับ ได้แก่:
    - Category 1: หมวดหมู่หลัก ได้แก่ หัตถการ / อสาการภาวะแทรกซ้อน / การปฏิบัติตัวหลังการทำหัตถการ
    - Category 2: หมวดย่อย เช่น pain, swelling, local anesthesia, oral hygiene ฯลฯ ซึ่งเป็น subset ของ Category 1
  - จากนั้นได้ดำเนินการดังนี้:
    - สร้างชุดคำถามที่มีการ label แล้ว ว่าคำถามแต่ละข้อเกี่ยวข้องกับ Category1 และ Category2 ใด,
    - สร้าง knowledge base ที่จัดเก็บเป็น chunks โดยแต่ละ chunk มี metadata ระบุ category1 และ category2 ชัดเจน,
    - ทดสอบระบบ RAG โดยส่งคำถามเข้าสู่ระบบ และบันทึก chunks ที่ถูกดึงออกมา,
    - ประเมินผล โดยตรวจสอบว่า chunk ที่ระบบดึงมาในอันดับต้น ๆ (Top‑k) มีหมวดหมู่ตรงกับที่ label ไว้หรือไม่,
  - ใช้เกณฑ์ เช่น Top‑K Accuracy, Precision/Recall ต่อ category, F1 score
  - <img width="1281" height="949" alt="image" src="https://github.com/user-attachments/assets/73479504-17f4-4906-a739-bb7dfa439617" />

