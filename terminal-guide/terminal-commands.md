# Terminal komandalari qo‘llanmasi

Bu qo‘llanmada terminal nima ekani va eng kerakli komandalar tushuntirilgan. Har bir komanda uchun vazifa, qachon ishlatilishi va amaliy misol berilgan.

## 1. Terminal nima?

**Ta’rif:** Terminal — kompyuter bilan matnli buyruqlar orqali muloqot qilish imkonini beradigan dastur yoki interfeys.

**Vazifasi:** Sichqoncha o‘rniga buyruq yozib, kompyuterga topshiriq berish.

## 2. Terminal nima uchun kerak?

**Ta’rif:** Fayl va papkalarni boshqarish, dasturlarni ishga tushirish, Git buyruqlarini bajarish va tizim bilan tez ishlash uchun kerak.

**Qachon ishlatiladi:** Dasturchilar Git, dasturlash tillari va ko‘plab vositalar bilan ishlaganda terminaldan foydalanadi.

## 3. pwd — joriy joylashuvni ko‘rish

**Vazifasi:** Joriy terminal qaysi papkada turganini to‘liq manzili bilan ko‘rsatadi.

**Qachon ishlatiladi:** Qayerda turganingizni bilmay qolganda.

```bash
pwd
```

## 4. ls — fayllarni ko‘rish

**Vazifasi:** Joriy papkadagi fayl va papkalar ro‘yxatini ko‘rsatadi. Windows PowerShell’da `ls` alias sifatida ishlaydi.

**Qachon ishlatiladi:** Papka ichida nimalar borligini bilish uchun.

```bash
ls
```

## 5. cd — papkaga kirish

**Vazifasi:** Ko‘rsatilgan papkaga o‘tadi.

**Qachon ishlatiladi:** Boshqa papkada ishlash kerak bo‘lganda.

```bash
cd documents
```

## 6. cd .. — yuqori papkaga chiqish

**Vazifasi:** Joriy papkaning bitta yuqori darajasiga qaytadi.

**Qachon ishlatiladi:** Ichki papkadan chiqib, ota papkaga qaytish uchun.

```bash
cd ..
```

## 7. mkdir — papka yaratish

**Vazifasi:** Yangi papka yaratadi.

**Qachon ishlatiladi:** Yangi loyiha yoki bo‘lim uchun papka kerak bo‘lganda.

```bash
mkdir my-folder
```

## 8. touch — fayl yaratish

**Vazifasi:** Git Bash, macOS va Linux’da yangi bo‘sh fayl yaratadi. PowerShell’da `New-Item notes.txt -ItemType File` ishlatilishi mumkin.

**Qachon ishlatiladi:** Yangi bo‘sh fayl kerak bo‘lganda.

```bash
touch notes.txt

# PowerShell varianti:
New-Item notes.txt -ItemType File
```
