# Git komandalari qo‘llanmasi

Bu qo‘llanmada Git asoslari va eng kerakli Git komandalari tushuntirilgan. Har bir mavzuda ta’rif, vazifa, qachon ishlatilishi va amaliy misol berilgan.

## 1. Git nima?

**Ta’rif:** Git — fayllardagi o‘zgarishlarni kuzatish va loyiha versiyalarini boshqarish uchun ishlatiladigan taqsimlangan versiya nazorati tizimi.

**Vazifasi:** Loyiha tarixini saqlaydi. Har bir o‘zgarish kim tomonidan va qachon qilingani yozib boriladi.

**Qachon ishlatiladi:** Dastur yozganda, hujjat tayyorlaganda yoki istalgan loyihada fayllarning eski holatlarini saqlab qo‘yish kerak bo‘lganda.

```bash
git --version
```

## 2. Git nima uchun kerak?

**Ta’rif:** Git o‘zgarishlar tarixini saqlash, oldingi holatlarga qaytish, xatolarni aniqlash, branchlarda alohida ishlash va jamoada hamkorlik qilish uchun kerak.

**Vazifasi:** Fayl nomlarini `loyiha_final`, `loyiha_final2` kabi ko‘paytirmasdan, hamma versiyani bitta joyda saqlaydi.

**Qachon ishlatiladi:** Loyiha ustida bir necha kun yoki bir necha kishi ishlaganda; yangi g‘oyani asosiy kodga tegmasdan sinab ko‘rmoqchi bo‘lganda.

```bash
git log --oneline
```

## 3. Repository nima?

**Ta’rif:** Repository — loyiha fayllari va ularning Git tarixini saqlaydigan joy. Lokal repository kompyuterda, remote repository esa GitHub kabi serverda bo‘lishi mumkin.

**Vazifasi:** Loyiha fayllarini va ularning butun tarixini bir joyda saqlaydi. Papka ichidagi yashirin `.git` papkasi shu tarixni ushlab turadi.

**Qachon ishlatiladi:** Har bir loyiha uchun alohida repository yaratiladi.

```bash
mkdir my-project
cd my-project
git init
```

## 4. Global va Local konfiguratsiya farqi

**Ta’rif:** Global sozlama foydalanuvchining barcha loyihalariga odatda tatbiq etiladi. Local sozlama faqat joriy repository uchun amal qiladi. Local qiymat mavjud bo‘lsa, shu repository’da global qiymatdan ustun turadi.

**Vazifasi:** Commit muallifi (ism va email) kimligini Gitga bildiradi.

**Qachon ishlatiladi:** Global — kompyuterda birinchi marta Git o‘rnatilganda. Local — ayrim loyihada boshqa ism yoki email ishlatish kerak bo‘lganda.

```bash
# Global
git config --global user.name "Ism Familiya"
git config --global user.email "email@example.com"

# Local (faqat joriy repository uchun)
git config user.name "Ism Familiya"
git config user.email "email@example.com"

# Sozlamalarni ko‘rish
git config --list
```

## 5. git init

**Ta’rif:** Joriy papkada yangi Git repository boshlaydi.

**Vazifasi:** Papka ichida `.git` yashirin papkasini yaratadi va shu papkani Git kuzata boshlaydi.

**Qachon ishlatiladi:** Yangi loyihani Git bilan kuzatishni boshlashda, bir marta.

```bash
git init
```

## 6. git status

**Ta’rif:** Repository holatini ko‘rsatadi.

**Vazifasi:** Yangi, o‘zgargan, stagingga qo‘shilgan va hali commit qilinmagan fayllarni ko‘rsatadi.

**Qachon ishlatiladi:** `git add` va `git commit` dan oldin va keyin, nima o‘zgarganini tekshirish uchun. Eng ko‘p ishlatiladigan komandalardan biri.

```bash
git status
git status --ignored
```

## 7. git add

**Ta’rif:** Tanlangan fayllardagi o‘zgarishlarni staging area’ga qo‘shadi.

**Vazifasi:** Qaysi o‘zgarishlar keyingi commitga kirishini tanlash bosqichi.

**Qachon ishlatiladi:** Commit qilishdan oldin. Bitta faylni qo‘shish uchun fayl nomi yoziladi, hammasini qo‘shish uchun `.` yoziladi.

```bash
git add README.md
git add .
```
