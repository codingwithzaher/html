# 🟠 المسارات واستخدام الصور في HTML

## 🔷 مفهوم مسار الملف:

**مسار الملف** هو العنوان الذي يُستخدم لتحديد مكان ملف معين داخل هيكلية المجلدات في النظام أو الموقع.

### هناك نوعان رئيسيان من مسارات الملفات:

1. **المسار الكامل (Absolute Path):** يحدد الموقع الكامل للملف بدءًا من جذر النظام أو الموقع.
2. **المسار النسبي (Relative Path):** يحدد الموقع النسبي للملف بالنسبة للمكان الذي يتم استدعاء الملف منه (مثل الصفحة الحالية).

## 🔶 أمثلة شاملة حول وضع مسارات نسبية:

المسارات النسبية تعتمد على مكان الملف الحالي بالنسبة إلى الملف المراد الوصول إليه.

1. **إذا كان ملف HTML والصورة في نفس المجلد:**

   ```html
   <img src="image.jpg" alt="صورة مثال" />
   ```

2. **إذا كانت الصورة موجودة في مجلد فرعي داخل المجلد الحالي:**

   ```html
   <img src="images/photo.jpg" alt="صورة داخل مجلد فرعي" />
   ```

3. **إذا كانت الصورة موجودة في المجلد العلوي بالنسبة لملف HTML:**

   ```html
   <img src="../photo.jpg" alt="صورة من المجلد العلوي" />
   ```

4. **إذا كانت الصورة موجودة في مجلد مختلف داخل مجلد علوي:**
   ```html
   <img src="../assets/images/photo.jpg" alt="صورة من مجلد آخر" />
   ```

## 🔶 أمثلة شاملة حول وضع مسارات كاملة:

المسار الكامل يحدد الموقع الكامل للملف، بغض النظر عن موقع الملف الحالي.

1. **استخدام رابط URL كامل:**

   ```html
   <img
     src="https://www.example.com/images/photo.jpg"
     alt="صورة من رابط كامل"
   />
   ```

2. **مسار كامل لنظام الملفات المحلي (على جهازك، غير مناسب للويب):**
   ```html
   <img
     src="C:/Users/UserName/Pictures/photo.jpg"
     alt="صورة من المسار الكامل للنظام"
   />
   ```

## 🔶 وضع نفس المسار بشكل كامل وبشكل نسبي:

1. **المسار الكامل:**

   ```html
   <img
     src="https://www.example.com/assets/images/photo.jpg"
     alt="صورة من رابط كامل"
   />
   ```

2. **المسار النسبي:**
   ```html
   <img src="assets/images/photo.jpg" alt="صورة من مسار نسبي" />
   ```

### 🔸 ملحوظة:

المسارات النسبية مفيدة في البيئات المحلية أو عندما يتم نقل الموقع بالكامل، بينما المسار الكامل يكون مناسبًا عند استدعاء موارد خارجية.

## 🔷 هل أستخدم المسار الكامل أو المسار النسبي؟

- **استخدام المسار النسبي** يُفضل عند العمل مع ملفات داخل موقع ويب واحد، مما يجعل الموقع أكثر مرونة ويسهل نقل الملفات والمجلدات.
- **المسار الكامل** يُستخدم عند الحاجة لاستدعاء موارد خارجية مثل ملفات على مواقع أخرى أو سيرفرات بعيدة.

## 🔷 أهمية الصور وأنواعها:

الصور تضيف جاذبية بصرية وشرحًا إضافيًا للمحتوى. **أنواع الصور الشائعة:**

1. **JPEG/JPG:** جيد للصور التي تحتوي على تدرجات ألوان مثل الصور الفوتوغرافية.
2. **PNG:** يدعم الشفافية، وهو مثالي للرموز والشعارات.
3. **GIF:** يُستخدم للصور المتحركة البسيطة.
4. **SVG:** مناسب للرسوميات المتجهة مثل الأيقونات والشعارات.
5. **WEBP:** تنسيق حديث يقدم جودة عالية مع حجم ملف أصغر.

## 🔶 إضافة صورة في الصفحة:

يمكنك إضافة صورة إلى صفحة HTML باستخدام وسم `<img>`.

```html
<img src="images/photo.jpg" alt="صورة وصفية" />
```

## 🔶 وضع نص بديل للصورة:

**النص البديل (alt)** يُستخدم كبديل للصورة في حال تعذر تحميلها أو عند استخدام برامج قراءة الشاشة للمستخدمين ذوي الاحتياجات الخاصة.

```html
<img src="images/photo.jpg" alt="صورة لشروق الشمس" />
```

## 🔶 تحديد حجم الصورة:

يمكنك تحديد عرض وارتفاع الصورة باستخدام سمات `width` و`height`.

```html
<img src="images/photo.jpg" alt="صورة وصفية" width="300" height="200" />
```

أو يمكنك تحديد الحجم باستخدام خاصية `style`:

```html
<img
  src="images/photo.jpg"
  alt="صورة وصفية"
  style="width: 300px; height: 200px;"
/>
```
