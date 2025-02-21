Git bilan samarali ishlash uchun eng muhim buyruqlar va ularning ishlatilishini quyida tushuntirib o'taman.  

---

## **1. Git boshlash va sozlash**  
🔹 **Git konfiguratsiyasi (faqat bir marta bajariladi)**  
```sh
git config --global user.name "Ismingiz"
git config --global user.email "Emailingiz"
```

🔹 **Yangi Git repository yaratish (loyihani Git bilan bog‘lash)**  
```sh
git init  
```

🔹 **GitHub-dagi repository bilan bog‘lash**  
```sh
git remote add origin https://github.com/FoydalanuvchiNomi/RepoNomi.git
```

---

## **2. Loyihani boshqarish (Fayllarni qo‘shish, commit qilish, yuborish)**  

🔹 **Barcha fayllarni kuzatuvga qo‘shish**  
```sh
git add .
```

🔹 **Agar faqat bitta faylni qo‘shmoqchi bo‘lsangiz**  
```sh
git add fayl_nomi
```

🔹 **O‘zgarishlarni commit qilish (saqlash)**  
```sh
git commit -m "O‘zgarish haqida izoh"
```

🔹 **O‘zgarishlarni GitHub-ga yuklash**  
```sh
git push origin main
```

🔹 **Agar repository hali "main" emas "master" bo‘lsa**  
```sh
git branch -M main
git push -u origin main
```

---

## **3. O‘zgarishlarni tekshirish va qaytarish**  

🔹 **Repositorydagi holatni tekshirish**  
```sh
git status
```

🔹 **Qanday o‘zgarishlar qilinganini ko‘rish**  
```sh
git diff
```

🔹 **Oxirgi commitdan keyingi o‘zgarishlarni bekor qilish**  
```sh
git checkout -- fayl_nomi
```

🔹 **Oxirgi commitni bekor qilish (lekin fayllar o‘zgarishsiz qoladi)**  
```sh
git reset HEAD~
```

🔹 **Oxirgi commitni butunlay o‘chirish (o‘zgarishlar ham yo‘qoladi!)**  
```sh
git reset --hard HEAD~
```

---

## **4. Tarmoqlar (Branches) bilan ishlash**  

🔹 **Yangi branch yaratish**  
```sh
git branch yangi_branch
```

🔹 **Branchlar ro‘yxatini ko‘rish**  
```sh
git branch
```

🔹 **Boshqa branchga o‘tish**  
```sh
git checkout yangi_branch
```

🔹 **Yangi branch yaratish va unga o‘tish**  
```sh
git checkout -b yangi_branch
```

🔹 **Branchni GitHub-ga yuklash**  
```sh
git push origin yangi_branch
```

🔹 **Branchni birlashtirish (merge)**  
```sh
git checkout main  
git merge yangi_branch
```

🔹 **Branchni o‘chirish (mahalliy)**  
```sh
git branch -d yangi_branch
```

🔹 **Branchni o‘chirish (GitHub-da)**  
```sh
git push origin --delete yangi_branch
```

---

## **5. Uzoqdagi (remote) repository bilan ishlash**  

🔹 **GitHub-dagi kodlarni olish (klonlash)**  
```sh
git clone https://github.com/FoydalanuvchiNomi/RepoNomi.git
```

🔹 **GitHub-dan o‘zgarishlarni yuklash**  
```sh
git pull origin main
```

🔹 **Agar `git pull` qilganda conflict chiqsa, avval lokal commit qilish kerak**  
```sh
git commit -m "Lokal o‘zgarishlar"
git pull origin main
```

🔹 **Agar boshqa tarmoqdan o‘zgarishlarni olish kerak bo‘lsa**  
```sh
git fetch origin branch_nomi
```

---

## **6. Commit tarixini ko‘rish va boshqarish**  

🔹 **Commit tarixini ko‘rish**  
```sh
git log
```

🔹 **Commitlarni qisqa ko‘rinishda chiqarish**  
```sh
git log --oneline --graph --all
```

🔹 **Oxirgi commitni o‘zgartirish (masalan, yozilgan izohni o‘zgartirish)**  
```sh
git commit --amend -m "Yangi commit xabari"
```

---

## **7. Git Ignore va tozalash**  

🔹 **Keraksiz fayllarni Git kuzatmasligi uchun `.gitignore` yaratish**  
```sh
touch .gitignore
echo "node_modules/" >> .gitignore
```

🔹 **Git cache-ni tozalash (ignore qilingan fayllarni o‘chirish)**  
```sh
git rm -r --cached .
git add .
git commit -m "Git ignore yangilandi"
```

---

## **8. Tag (versiyalar) bilan ishlash**  

🔹 **Tag yaratish**  
```sh
git tag v1.0
```

🔹 **Taglar ro‘yxatini ko‘rish**  
```sh
git tag
```

🔹 **GitHub-ga tagni yuklash**  
```sh
git push origin v1.0
```

🔹 **Tagni o‘chirish**  
```sh
git tag -d v1.0
git push origin --delete v1.0
```

---

## **Xulosa**  
Agar siz Git bilan samarali ishlashni xohlasangiz, quyidagi amallarni doimiy bajarib borishingiz kerak:  

✅ **Har doim commit qilish va push qilishni unutmaslik**  
✅ **Branchlar bilan ishlashni o‘rganish**  
✅ **Git status va git log orqali loyihani nazorat qilish**  
✅ **Agar conflict bo‘lsa, xotirjam hal qilish**

Agar bularni bilmasangiz yaxshigina yeysiz from Dilshod teacher 😊