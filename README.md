# 🎬 ReelsBot AI — APK Build Guide

## วิธี Build APK ผ่าน GitHub Actions (บนมือถือ 100%)

---

## ขั้นตอนที่ 1 — สร้าง GitHub Account
1. เปิด Browser บนมือถือ
2. ไปที่ **github.com**
3. กด **Sign up** → สมัครฟรี

---

## ขั้นตอนที่ 2 — Upload โค้ด

### วิธีที่ง่ายที่สุด (บนมือถือ):
1. กด **+** → **New repository**
2. ตั้งชื่อ: `reelsbot-apk`
3. เลือก **Public**
4. กด **Create repository**
5. กด **uploading an existing file**
6. Upload ไฟล์ทั้งหมดในโฟลเดอร์นี้

### โครงสร้างที่ต้อง Upload:
```
.github/workflows/build.yml
app/src/main/AndroidManifest.xml
app/src/main/assets/index.html
app/src/main/java/com/reelsbot/MainActivity.java
app/src/main/java/com/reelsbot/SchedulerService.java
app/src/main/java/com/reelsbot/BootReceiver.java
app/src/main/res/values/strings.xml
app/src/main/res/values/styles.xml
app/build.gradle
build.gradle
settings.gradle
gradlew
gradle/wrapper/gradle-wrapper.properties
```

---

## ขั้นตอนที่ 3 — รอ Build อัตโนมัติ

หลัง Upload เสร็จ GitHub Actions จะ build อัตโนมัติ:

1. ไปที่ tab **Actions** บน GitHub
2. ดู workflow **Build ReelsBot APK**
3. รอประมาณ **5-10 นาที**
4. พอขึ้น ✅ กด **Artifacts** → **ReelsBot-APK**
5. Download → ได้ไฟล์ `app-debug.apk`

---

## ขั้นตอนที่ 4 — ติดตั้ง APK

1. เปิดไฟล์ `app-debug.apk` บนมือถือ
2. ถ้ามีข้อความ "Unknown sources" → ไป Settings → Security → เปิด **Install unknown apps**
3. กด **Install**
4. เปิดแอพ **ReelsBot AI** จาก Home Screen 🎉

---

## Build ใหม่อัตโนมัติทุกครั้งที่แก้ไข

ถ้าต้องการแก้ไข `index.html` (เพิ่มฟีเจอร์):
1. ไปที่ `app/src/main/assets/index.html` บน GitHub
2. กด **Edit** (ดินสอ)
3. แก้ไข → กด **Commit**
4. GitHub Actions จะ Build APK ใหม่อัตโนมัติ!

---

## ฟีเจอร์ใน APK

- 🎬 สร้าง Reels อัตโนมัติด้วย Gemini / Grok
- 🎨 10 Video Styles
- ⏱️ Custom Duration (1วิ - 60นาที)
- ⏰ Schedule โพสต์อัตโนมัติ
- 🚀 Auto-post TikTok / Facebook / YouTube
- 📱 Background Service (ทำงานแม้ปิดหน้าจอ)
- 🔄 Auto-start ตอนบูตมือถือ
