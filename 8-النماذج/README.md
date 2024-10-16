# 🔷 مفهوم النموذج (Form) في HTML

**النموذج (Form)** هو عنصر في HTML يسمح للمستخدمين بإدخال البيانات وإرسالها إلى الخادم. يتم استخدام النماذج عادةً في صفحات الويب لجمع المعلومات، مثل اسم المستخدم، كلمة المرور، أو بيانات أخرى.

## 🔶 إضافة نموذج في الصفحة

لإضافة نموذج إلى صفحة HTML، نستخدم وسم `<form>`. يمكنك وضع حقول الإدخال المختلفة مثل النصوص، الأزرار، أو مربعات الاختيار بداخل هذا الوسم.

```html
<form>
  <!-- حقول الإدخال ستكون هنا -->
</form>
```

## 🔶 إضافة زر لإرسال محتوى النموذج

لإضافة زر يتيح للمستخدم إرسال البيانات المدخلة في النموذج إلى الخادم، نستخدم وسم `<button>` أو `<input type="submit">`.

```html
<form>
  <input type="text" name="username" placeholder="أدخل اسم المستخدم" />
  <button type="submit">إرسال</button>
</form>
```

## 🔶 تحديد أسلوب إرسال بيانات النموذج

يمكنك تحديد الطريقة التي سيتم بها إرسال البيانات عبر سمة `method`، وهي إما:

- **GET:** يتم إرسال البيانات كجزء من رابط الصفحة.
- **POST:** يتم إرسال البيانات بشكل مخفي في جسم الطلب (يُفضل للأمان).

```html
<form method="post">
  <input type="text" name="username" placeholder="أدخل اسم المستخدم" />
  <button type="submit">إرسال</button>
</form>
```

## 🔶 إعطاء أسماء للوسوم الموضوعة في النموذج

يجب أن تُعطى الوسوم داخل النموذج سمة `name` لتحديد البيانات التي سيتم إرسالها عند تقديم النموذج.

```html
<form>
  <input type="text" name="username" placeholder="أدخل اسم المستخدم" />
  <input type="password" name="password" placeholder="أدخل كلمة المرور" />
  <button type="submit">إرسال</button>
</form>
```

## 🔶 تحديد أين سيتم إرسال محتوى النموذج

يتم استخدام سمة `action` لتحديد الصفحة أو العنوان (URL) الذي سيتم إرسال بيانات النموذج إليه.

```html
<form action="/submit-form" method="post">
  <input type="text" name="username" placeholder="أدخل اسم المستخدم" />
  <button type="submit">إرسال</button>
</form>
```

## 🔶 تفعيل الإكمال التلقائي في النموذج

يمكنك تمكين أو تعطيل خاصية **الإكمال التلقائي** عبر سمة `autocomplete` في وسم `<form>`.

```html
<form autocomplete="on">
  <input type="text" name="username" placeholder="أدخل اسم المستخدم" />
  <button type="submit">إرسال</button>
</form>
```

## 🔶 إلغاء التدقيق على القيم المدخلة في النموذج

يمكنك إلغاء **التدقيق (Validation)** على القيم المدخلة عبر إضافة سمة `novalidate` إلى وسم `<form>`.

```html
<form action="/submit-form" method="post" novalidate>
  <input type="email" name="email" placeholder="أدخل البريد الإلكتروني" />
  <button type="submit">إرسال</button>
</form>
```

## 🔶 تحديد أين سيتم فتح الصفحة التي تستقبل بيانات النموذج

يمكنك التحكم بمكان فتح الصفحة التي تستقبل البيانات عبر سمة `target`. على سبيل المثال، لفتح الصفحة في نافذة جديدة:

```html
<form action="/submit-form" method="post" target="_blank">
  <input type="text" name="username" placeholder="أدخل اسم المستخدم" />
  <button type="submit">إرسال</button>
</form>
```

## 🔶 أهم الوسوم التي تستخدم مع النماذج

1. `<input>:` لإدخال البيانات.

   - `type="text"`: إدخال نص.
   - `type="password"`: إدخال كلمة مرور.
   - `type="email"`: إدخال بريد إلكتروني.
   - `type="submit"`: زر إرسال.
   - `type="radio"`: زر اختيار دائري.
   - `type="checkbox"`: مربع اختيار.
   - `type="file"`: رفع ملف.

2. `<textarea>:` لإدخال نص متعدد الأسطر.

```html
<textarea name="message" placeholder="اكتب رسالتك هنا"> </textarea>
```

3. `<select>:` قائمة منسدلة.

```html
<select name="country">
  <option value="SA">السعودية</option>
  <option value="EG">مصر</option>
</select>
```

4. `<button>:` زر عام يمكن تخصيصه.

```html
<button type="submit">إرسال</button>
```

5. `<label>:` وسم لتعريف الحقول.

```html
<label for="username">اسم المستخدم:</label>
<input type="text" id="username" name="username" />
```
