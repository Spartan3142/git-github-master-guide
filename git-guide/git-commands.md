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

## 8. git commit

**Ta’rif:** Staging area’dagi o‘zgarishlarni repository tarixida yangi commit sifatida saqlaydi.

**Vazifasi:** Loyihaning shu paytdagi holatini xabar bilan birga saqlab qo‘yadi. Xabar o‘zgarish mazmunini qisqa ifodalashi kerak.

**Qachon ishlatiladi:** Bitta ish tugagandan keyin (masalan, bitta bo‘lim yozilgach).

```bash
git add .
git commit -m "Add project files"
```

## 9. git log

**Ta’rif:** Repository’dagi commitlar tarixini ko‘rsatadi.

**Vazifasi:** Muallif, sana va commit xabarlarini ko‘rsatadi. `--oneline` har bir commitni bitta qatorda chiqaradi.

**Qachon ishlatiladi:** Oldin nima qilinganini ko‘rish yoki commit yaratilganini tekshirish uchun.

```bash
git log
git log --oneline
```

## 10. git branch

**Ta’rif:** Branchlarni ko‘rish, yangi branch yaratish va boshqarish uchun ishlatiladi.

**Vazifasi:** Branch — loyihaning alohida ish yo‘nalishi. Bu `main` ga tegmasdan ishlash imkonini beradi.

**Qachon ishlatiladi:** Mavjud branchlar ro‘yxatini ko‘rish yoki yangi branch yaratish kerak bo‘lganda.

```bash
git branch
git branch new-feature
```

## 11. git switch

**Ta’rif:** Mavjud branchga o‘tadi. `-c` bilan yangi branch yaratib, unga bir vaqtda o‘tish mumkin.

**Vazifasi:** Branchlar orasida almashish.

**Qachon ishlatiladi:** Boshqa branchda ishlash kerak bo‘lganda yoki yangi mavzu uchun branch ochganda.

```bash
git switch main
git switch -c new-feature
```

## 12. git merge

**Ta’rif:** Boshqa branchdagi o‘zgarishlarni joriy branchga birlashtiradi.

**Vazifasi:** Alohida branchda bajarilgan ishni asosiy branchga qo‘shadi. Merge qilishdan oldin natija qabul qilinadigan branchga o‘tiladi.

**Qachon ishlatiladi:** Branchdagi ish tayyor bo‘lgach. (Bu topshiriqda merge’ni keyingi darsda o‘qituvchi ko‘rsatadi.)

```bash
git switch main
git merge new-feature
```

## 13. git branch -d

**Ta’rif:** Lokal branchni o‘chiradi.

**Vazifasi:** Odatda birlashtirilgan branchni xavfsiz o‘chirish uchun ishlatiladi. Merge qilinmagan ish bo‘lsa, Git ogohlantiradi.

**Qachon ishlatiladi:** Branchdagi ish `main` ga qo‘shilgandan keyin, keraksiz branchni tozalash uchun.

```bash
git switch main
git branch -d new-feature
```

---

## Savol va javoblar

**1. `git add` va `git commit` nima uchun alohida?**
`git add` qaysi o‘zgarishlar commitga kirishini tanlaydi. `git commit` esa tanlanganlarni tarixga saqlaydi. Shu sababli bir nechta fayl o‘zgargan bo‘lsa ham, faqat kerakli qismni commit qilish mumkin.

**2. Commit nima?**
Commit — loyiha holatining saqlangan nusxasi. Unda o‘zgarishlar, muallif, sana va xabar bor. Kerak bo‘lsa, shu holatga qaytish mumkin.

**3. `git add README.md` bilan `git add .` ning farqi nima?**
Birinchisi faqat `README.md` ni qo‘shadi. Ikkinchisi joriy papkadagi barcha o‘zgargan va yangi fayllarni qo‘shadi (`.gitignore` dagilardan tashqari).

**4. Branch nima uchun kerak?**
Branch asosiy kodga tegmasdan yangi ishni alohida joyda bajarish imkonini beradi. Ish tayyor bo‘lgach, uni `main` ga birlashtirish mumkin.

**5. `.gitignore` nima uchun kerak?**
U Git kuzatmasligi kerak bo‘lgan vaqtinchalik yoki shaxsiy fayllarni (masalan, `*.tmp`, `private-notes.txt`) belgilaydi, shuning uchun ular tasodifan commit qilinmaydi.
