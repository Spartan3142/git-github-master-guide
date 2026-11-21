# GitHub komandalari qo‘llanmasi

Bu qo‘llanmada GitHub platformasi, remote repository va unga oid komandalar tushuntirilgan.

## 1. GitHub nima?

**Ta’rif:** GitHub — Git repository’larini internetda saqlash, ulashish, ko‘rib chiqish va loyihalar ustida hamkorlik qilish platformasi.

**Vazifasi:** Loyihani onlayn saqlaydi, shuning uchun kompyuter buzilsa ham ish yo‘qolmaydi va uni boshqalarga ko‘rsatish mumkin.

## 2. Git va GitHub farqi

**Ta’rif:** Git — kompyuterda ham ishlaydigan versiya nazorati tizimi. GitHub — Git repository’larini onlayn saqlash va boshqarish xizmati.

**Vazifasi:** Git tarixni yuritadi, GitHub esa shu tarixni internetda saqlaydi va hamkorlikni osonlashtiradi. Git GitHub’siz ham ishlaydi.

## 3. GitHub account nima?

**Ta’rif:** GitHub account — foydalanuvchining GitHub’dagi shaxsiy hisobi.

**Vazifasi:** Repository yaratish, loyihalarni saqlash va platformadan foydalanish uchun kerak. Account `github.com` saytida ro‘yxatdan o‘tish orqali ochiladi.

## 4. Repository nima?

**Ta’rif:** GitHub repository — loyiha fayllari, commitlar, branchlar va boshqa loyiha ma’lumotlari saqlanadigan masofaviy ombor.

**Vazifasi:** Lokal repository’ning onlayn nusxasi sifatida xizmat qiladi.

## 5. Public va Private repository farqi

**Ta’rif:** Public repository internetdagi hammaga ko‘rinadi. Private repository faqat egasi va ruxsat berilgan foydalanuvchilarga ko‘rinadi.

**Qachon ishlatiladi:** Hammaga ko‘rsatiladigan loyihalar uchun Public, maxfiy ishlar uchun Private tanlanadi. Parol va tokenlarni hech qachon repository’ga yozmaslik kerak.

## 6. Remote nima?

**Ta’rif:** Remote — lokal Git repository bilan bog‘langan masofaviy repository manzili. Ko‘pincha GitHub’dagi repository remote sifatida ulanadi.

**Vazifasi:** Lokal repository qayerga push qilishni va qayerdan pull qilishni biladi. Odatda asosiy remote `origin` deb nomlanadi.

## 7. git remote add

**Ta’rif:** Mavjud lokal repository’ga remote manzil qo‘shadi. `origin` odatda asosiy remote uchun ishlatiladigan nom.

**Vazifasi:** Lokal loyihani GitHub’dagi repository bilan bog‘laydi.

**Qachon ishlatiladi:** Lokalda `git init` qilingan loyihani GitHub’ga birinchi marta ulashda.

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

## 8. git remote -v

**Ta’rif:** Ulangan remote repository’larning fetch va push manzillarini ko‘rsatadi.

**Qachon ishlatiladi:** Remote to‘g‘ri ulanganini tekshirish uchun.

```bash
git remote -v
```
