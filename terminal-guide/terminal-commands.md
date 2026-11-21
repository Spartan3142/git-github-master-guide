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

## 9. cat — fayl mazmunini ko‘rish

**Vazifasi:** Matnli fayl ichidagi yozuvlarni terminalda chiqaradi.

**Qachon ishlatiladi:** Faylni ochmasdan ichini tez ko‘rish uchun.

```bash
cat notes.txt
```

## 10. clear — terminalni tozalash

**Vazifasi:** Terminal oynasidagi avvalgi matnlarni ekrandan tozalaydi. Fayllarni o‘chirmaydi.

**Qachon ishlatiladi:** Ekran to‘lib ketganda.

```bash
clear
```

## 11. cp — nusxa olish

**Vazifasi:** Fayl yoki papkadan nusxa yaratadi.

**Qachon ishlatiladi:** Faylning zaxira nusxasi kerak bo‘lganda.

```bash
cp notes.txt notes-copy.txt
```

## 12. mv — ko‘chirish yoki nomini o‘zgartirish

**Vazifasi:** Fayl yoki papkani boshqa joyga ko‘chiradi yoki nomini o‘zgartiradi.

**Qachon ishlatiladi:** Faylni boshqa papkaga o‘tkazish yoki nomini almashtirish kerak bo‘lganda.

```bash
mv old.txt new.txt
```

## 13. rm — fayl o‘chirish

**Vazifasi:** Ko‘rsatilgan faylni o‘chiradi. Faqat mashq uchun yaratilgan faylda ehtiyotkorlik bilan ishlating.

**Qachon ishlatiladi:** Keraksiz sinov faylini olib tashlash uchun.

```bash
rm notes-copy.txt
```

> Xavfsizlik: `rm` faylni o‘chiradi va qaytarib bo‘lmaydi. Faqat o‘zingiz yaratgan sinov fayllarini o‘chiring. `rm -rf` kabi xavfli buyruqlarni ishlatmang.

## 14. git init — repository yaratish

**Vazifasi:** Joriy papkada yangi Git repository boshlaydi.

**Qachon ishlatiladi:** Yangi loyihani Git bilan kuzatishni boshlashda.

```bash
mkdir my-project
cd my-project
git init
```

## 15. git status — Git holatini tekshirish

**Vazifasi:** Git repository’dagi yangi, o‘zgargan va stagingga qo‘shilgan fayllar holatini ko‘rsatadi.

**Qachon ishlatiladi:** Commit qilishdan oldin va keyin, nima o‘zgarganini ko‘rish uchun.

```bash
git status
```
