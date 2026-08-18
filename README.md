# รายงานการส่งการบ้าน: Agentic RAG (4-Hour Homework)

**ข้อมูลนักศึกษา:**
* **ชื่อ-นามสกุล:** สนธิ อิทธิพร
* **รหัสนักศึกษา:** 6730406372
* **ระดับที่เลือก:** ง่าย

---

## 📌 สรุปสิ่งที่เรียนรู้
1. **การสร้าง RAG Agent และ Custom Tools:** ได้เรียนรู้การเชื่อมต่อ Qdrant Vector Database เข้ากับ LlmAgent ผ่าน FunctionTool เพื่อให้ Agent ดึงข้อมูลบริบท (Context) มาตอบคำถามได้อย่างแม่นยำ
2. **การประเมินผลด้วย LLM-as-Judge:** ได้ทดลองใช้ Gemini เป็นผู้ประเมินคุณภาพคำตอบ (Score 1-5) พร้อมให้เหตุผลแบบโครงสร้าง JSON
3. **การรับมือกับ API Quotas & Rate Limits:** ได้เรียนรู้การแก้ปัญหา HTTP 429 (Resource Exhausted) โดยการจัดการคำสั่งด้วยการหน่วงเวลา (`asyncio.sleep`) และการเลือกรุ่นโมเดลที่เหมาะสม (`gemini-2.5-flash`)

---

## 📊 ผลเซลล์ "ตรวจสอบคำตอบ" (Self-Check Verification)
```text
🤖 Agent: เทคนิคการสร้างคำตอบจากข้อมูลที่ค้นพบ...
❓ Embedding คืออะไร? -> ⭐ 5/5
❓ ทำไม RAG ถึงสำคัญ? -> ⭐ 5/5

✅ Step 1 passed!
✅ Step 2 passed!
✅ Step 3 passed: ตอบครบ 3 ข้อ + LLM-as-Judge เสร็จ!
