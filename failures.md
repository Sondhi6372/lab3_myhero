### 2. `failures.md`

```markdown
# บันทึกข้อผิดพลาดและการแก้ไข (Failures Log)

| Query / สถานการณ์ที่พัง | Error Trace / Log ย่อ | ชนิดความผิดพลาด | การแก้ไข (Before / After) |
| :--- | :--- | :--- | :--- |
| การตั้งค่า API Key ล้มเหลว | `ClientError: 401 UNAUTHENTICATED` | Authentication Error | **Before:** ป้อนค่า Token ผิดพลาดลงในช่อง `input()` <br>**After:** ปรับโค้ดให้ตรวจสอบ `AIzaSy...` และดึงจาก `os.environ` ให้ถูกต้อง |
| ยิงคำถาม 3 ข้อติดกันใน Step 3 | `ClientError: 429 RESOURCE_EXHAUSTED` | Rate Limit / Quota Exceeded | **Before:** วนลูปถามทันทีทำให้ติด Free Tier Limit<br>**After:** เพิ่ม `await asyncio.sleep(10)` ระหว่างข้อ และเปลี่ยนมาใช้โมเดล `gemini-2.5-flash` |
