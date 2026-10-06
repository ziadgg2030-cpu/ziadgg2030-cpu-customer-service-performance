# تشغيل المشروع مجانًا على GitHub Pages

1. أنشئ Repository جديدًا على GitHub، مثل:
   `customer-service-performance`
2. ارفع محتويات هذا المشروع إلى الفرع `main`.
3. من GitHub افتح:
   **Settings → Pages**
4. في **Build and deployment** اختر **GitHub Actions**.
5. ادخل إلى تبويب **Actions** وانتظر انتهاء:
   `Deploy Customer Service Performance to GitHub Pages`
6. بعد نجاح الـworkflow سيظهر لك رابط الموقع في:
   **Settings → Pages → Visit site**

ملاحظات:
- الـFrontend مبني باستخدام React + Vite.
- GitHub Pages يستضيف الواجهة فقط، وليس الـAPI أو قاعدة البيانات.
- إذا كانت الواجهة تعتمد على API محلي/خاص، ستحتاج نشر الـAPI في خدمة أخرى وتحديد عنوانه في إعدادات المشروع.
- الـworkflow يبني فقط حزمة `@workspace/service-performance` لتكون المعاينة سريعة وبسيطة.
