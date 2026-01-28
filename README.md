# Web App

โปรเจกต์เว็บแอปพลิเคชัน

## การติดตั้ง

```bash
npm install
```

## การใช้งาน

```bash
npm start
```

## การเชื่อมต่อ GitHub

1. สร้าง repository ใหม่บน GitHub
2. เพิ่ม remote repository:
   ```bash
   git remote add origin https://github.com/USERNAME/REPO_NAME.git
   ```
3. Push code ไปยัง GitHub:
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git push -u origin main
   ```

## การเชื่อมต่อ Netlify

โปรเจกต์มีไฟล์ `netlify.toml` สำหรับตั้งค่า build และ deploy บน Netlify แล้ว

### ขั้นตอนการเชื่อมต่อ

1. **เข้าหน้า Netlify**  
   ไปที่ [https://app.netlify.com](https://app.netlify.com) แล้วลงชื่อเข้าใช้ (หรือสมัครด้วยบัญชี GitHub)

2. **เพิ่ม site จาก Git**
   - กด **"Add new site"** → **"Import an existing project"**
   - เลือก **GitHub** แล้วอนุญาต Netlify เข้าถึง repository

3. **เลือก repository**
   - เลือก `tamaketing/free-Quotation` (หรือชื่อ repo จริงของคุณ)
   - Branch: **main**

4. **ตั้งค่า Build (ถ้า Netlify ไม่อ่านจาก netlify.toml อัตโนมัติ)**
   - **Build command:** `npm run build` (หรือตามที่กำหนดในโปรเจกต์)
   - **Publish directory:** `dist` (หรือ `build` / `public` ตามที่โปรเจกต์ใช้)

5. กด **"Deploy site"**  
   Netlify จะ build และ deploy ทุกครั้งที่คุณ push ขึ้น GitHub

### หลังเชื่อมต่อแล้ว

- ดู URL ของ site ได้ที่ **Site overview** → **Domain management**
- แก้ไข `netlify.toml` ได้ตาม build command และโฟลเดอร์ที่โปรเจกต์ใช้จริง
