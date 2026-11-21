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

## 9. git push

**Ta’rif:** Lokal commitlarni remote repository’ga yuboradi.

**Vazifasi:** Kompyuterdagi ishni GitHub’ga yuklaydi. Birinchi pushda `-u` bilan upstream branch belgilanadi, keyin faqat `git push` yozish yetadi.

**Qachon ishlatiladi:** Commit qilingandan keyin ishni GitHub’ga yuborish kerak bo‘lganda.

```bash
git push -u origin github-guide
```

## 10. git pull

**Ta’rif:** Remote repository’dagi yangilanishlarni olib keladi va joriy branchga birlashtiradi.

**Qachon ishlatiladi:** Ishni boshlashdan oldin, GitHub’dagi eng yangi holatni olish uchun.

```bash
git pull origin main
```

## 11. git clone

**Ta’rif:** Masofaviy repository’ning nusxasini kompyuterga yuklab, lokal Git repository yaratadi.

**Qachon ishlatiladi:** GitHub’dagi loyihani yangi kompyuterga olish yoki boshqaning ochiq loyihasini yuklab olish uchun.

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

## 12. GitHub’da branch nima?

**Ta’rif:** GitHub’dagi branch — repository ichidagi alohida ish yo‘nalishi.

**Vazifasi:** `main` branchni darhol o‘zgartirmasdan vazifa bajarishga yordam beradi. GitHub’da branchlarni tepadagi branch tanlash menyusidan ko‘rish va almashtirish mumkin.

## 13. GitHub’da commit nima?

**Ta’rif:** Commit — repository tarixidagi saqlangan o‘zgarishlar to‘plami.

**Vazifasi:** GitHub’da commit xabari, muallifi, sanasi va o‘zgarishlar tafsilotini ko‘rish mumkin (`Commits` bo‘limida).

## 14. GitHub’da faylni tahrirlash

**Ta’rif:** Repository ichida faylni ochib, `Edit` (qalam) tugmasi orqali matnni o‘zgartirish va `Commit changes` orqali saqlash mumkin.

**Muhim:** O‘zgarishni to‘g‘ri branchga kiritish kerak. Aks holda boshqa branchdagi ishga halaqit berishi mumkin.

## 15. GitHub’da branchni o‘chirish

**Ta’rif:** Repository’ning `Branches` sahifasida branchni o‘chirish mumkin. Odatda ish merge qilingandan keyin branch o‘chiriladi.

**Terminal orqali:** Remote branchni terminaldan ham o‘chirish mumkin.

```bash
git push origin --delete branch-name
```

> Diqqat: bu topshiriqda branchlar o‘chirilmaydi. Bu faqat nazariy ma’lumot.

---

## GitHub’da yangi repository yaratish (5 bosqich)

1. **Kirish:** `github.com` ga kirib, o‘z account’ingizga login qiling.
2. **Yangi repository:** O‘ng yuqoridagi `+` belgisini bosing va `New repository` ni tanlang.
3. **Nom berish:** `Repository name` maydoniga `git-github-master-guide` deb yozing.
4. **Sozlamalar:** `Public` yoki `Private` ni tanlang. Lokalda README bor bo‘lsa, `Add a README file`, `.gitignore` va license kataklarini belgilamang.
5. **Yaratish:** `Create repository` tugmasini bosing va chiqqan repository manzilini (URL) nusxalab oling.

---

## Savol va javoblar

**1. Git va GitHub bir narsami?**
Yo‘q. Git — kompyuterdagi versiya nazorati dasturi. GitHub — Git repository’larini internetda saqlaydigan xizmat.

**2. `git push` va `git pull` o‘rtasidagi farq nima?**
`push` lokal commitlarni GitHub’ga yuboradi. `pull` GitHub’dagi yangilanishlarni kompyuterga olib keladi.

**3. `git clone` nima qiladi?**
GitHub’dagi repository’ning to‘liq nusxasini (fayllar va tarix bilan) kompyuterga yuklaydi.

**4. `origin` nima?**
`origin` — remote repository uchun odatda ishlatiladigan standart nom. Bu GitHub’dagi repository manzilining qisqa nomi.

**5. Public va Private repository farqi nima?**
Public hammaga ko‘rinadi, Private esa faqat egasi va ruxsat berilgan foydalanuvchilarga.
