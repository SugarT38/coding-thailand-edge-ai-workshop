<!-- workshop-header -->
<img width="1347" height="127" alt="Coding Thailand 2026 header" src="https://github.com/user-attachments/assets/ba5cf267-f460-4fb0-b69b-c461ae061a3b" />

# 📝 Worksheet W2 — Data Collection Log

> **ทำในช่วง 10:30-12:00**
> บันทึก process ของการเก็บข้อมูล

---

## ข้อมูลทีม + Edge Impulse

- **ชื่อทีม:** พรยังไม่รู้แต่เดี๋ยวรู้เอง
- **Edge Impulse Project URL:**
  ```
  https://studio.edgeimpulse.com/studio/1012061/impulse/1/learning/keras-transfer-kws/5
  ```

---

## 1. Setup Log

ก่อนเริ่มเก็บข้อมูล ทีมทำอะไรบ้าง?

| เวลา | ทำอะไร | ผู้รับผิดชอบ |
|---|---|---|
| 10:30 |ต่อบอร์ด|ทุกคน |
| 10.50 |เลือก Modul ที่สนใจ |ทุกคน |
| 11.00 |ออกแบบผลงาน |ทุกคน |
| 11.05 |ต่อ Modul และวางโค้ด | แอมและพลอย |
| 13.00 |เขียนโปรมแกรมการการต่อเซอเซอร์เสียงและบันทึกเสียง |เนย|
---

## 2. Data Collection Sessions

บันทึกแต่ละ session การเก็บข้อมูล:

### Session 1

- **เวลา:** 13.00 น. ถึง 13.20 น.
- **Class:** _________________
- **จำนวน samples ที่เก็บ:** 50
- **สภาพแวดล้อม:** มีเสียงรบกวน
- **ใครเป็น subject?:** แอมและพลอย
- **Variation ที่ลอง:** ได้ไฟล์เสียง
- **ปัญหาที่เจอ:** เสียงรบกวน

### Session 2

- **เวลา:** 13.30 ถึง 13.55 น.
- **Class:** _________________
- **จำนวน samples ที่เก็บ:** 50
- **สภาพแวดล้อม:** มีเสียงรบกวน
- **ใครเป็น subject?:** แอมและพลอย
- **Variation ที่ลอง:** ได้ไฟล์เสียง
- **ปัญหาที่เจอ:** เสียงรบกวน

### Session 3

- **เวลา:** _____ ถึง _____
- **Class:** _________________
- **จำนวน samples ที่เก็บ:** _____
- **สภาพแวดล้อม:** _________________
- **ใครเป็น subject?:** _________________
- **Variation ที่ลอง:** _________________
- **ปัญหาที่เจอ:** _________________

> หาก session มากกว่า 3 ให้ copy template เพิ่ม

---

## 3. Dataset Summary

| Class | จำนวน Train | จำนวน Test | สัดส่วน Train:Test |
| happy | 3 | 3 |84.0:16.0 |
| hello | 4 | 4 |19.4:80.8 |


| **รวม** |7|7|- |

**เป้าหมายตาม W1:** _______ samples × class
**ทำได้จริง:** _______ samples × class
**ห่างจากเป้า:** _______%

---

## 4. Quality Check

ตอบทุกข้อก่อนเริ่ม train:

- [ ] ทุก class มี samples ใกล้เคียงกัน (ไม่ต่างกันเกิน 20%)
- [ ] เก็บใน ≥2 สภาพแวดล้อม
- [ ] เก็บจาก ≥2 subjects (Vision/Audio/Motion ที่มีคน)
- [ ] มี variation ใน angle/distance/lighting
- [ ] ไม่มี mislabeled data (เช็คตัวอย่างแล้ว)
- [/ ] Train:Test split = 80:20

---

## 5. Reflection — สิ่งที่เรียนรู้

### a) สิ่งที่ยากที่สุด:
```
[การบันทึกเสียงและการรันโปรแกรมที่อินเทอร์เน็ตไม่อำนวย]
```

### b) ถ้าทำใหม่จะปรับอะไร:
```
[ความคมชัดของไฟล์เสียงที่อัด]
```

### c) คาดการณ์: model จะ confuse class ไหนกับอะไรมากที่สุด?
```
[สามารถแยกเสียงได้]
```

---

## 📤 วิธี submit

```bash
git add worksheets/W2-data-collection-log.md
git commit -m "docs: data collection log เก็บได้ครบ X samples ใน Y session"
git push
```

---

## 💡 Best Practices

1. **อย่าเก็บข้อมูลที่ "สมบูรณ์แบบ" หมด** — โลกจริงไม่สมบูรณ์แบบ
2. **เก็บข้อมูล "เหมือนไม่ใช่ class ใดเลย" เป็นอีก class** = noise/background class
3. **สลับคนเก็บ** — กัน bias ของ subject เดียว
4. **เช็คตัวอย่างทุก 20 samples** — กัน mislabel
