# Budgy

تطبيق ميزانية شخصية — واجهة عربي (RTL)، مبني كملف HTML واحد، ومربوط بـ Firebase (Authentication + Firestore) عشان بياناتك تتزامن لحظيًا على أي جهاز تدخل بيه (كمبيوتر أو موبايل) من نفس الحساب.

## النشر عن طريق GitHub Pages

1. ارفع هذا الريبو (أو المجلد ده) على GitHub.
2. من إعدادات الريبو: **Settings → Pages**.
3. تحت "Build and deployment"، اختار **Source: Deploy from a branch**.
4. اختار الفرع `main` والمجلد `/ (root)`، واحفظ.
5. بعد دقيقة أو اتنين، هيديك GitHub لينك بالشكل:
   `https://<username>.github.io/<repo-name>/`
6. افتح اللينك ده من أي جهاز — هيشتغل التطبيق مباشرة، من غير ما تحتاج ترجع لجهاز معين.

## تحديث التطبيق مستقبلًا

أي تعديل تحتاجه، كل اللي عليك تعمله:
1. عدّل ملف `index.html` (أو استبدله بنسخة جديدة).
2. ارفعه (commit + push) على نفس الفرع `main`.
3. GitHub Pages هيحدّث اللينك تلقائيًا خلال دقيقة أو اتنين — من غير أي خطوة تانية.

## مهم: Firebase Authorized Domains

عشان تسجيل الدخول يشتغل من اللينك بتاع GitHub Pages، لازم تضيف الدومين بتاعه في Firebase:

1. روح على [Firebase Console](https://console.firebase.google.com) → مشروع `budgy-7070`.
2. **Authentication → Settings → Authorized domains**.
3. دوس **Add domain** وضيف: `<username>.github.io`
4. احفظ.

من غير الخطوة دي، تسجيل الدخول/الحساب الجديد هيرفض يشتغل من لينك GitHub Pages.
