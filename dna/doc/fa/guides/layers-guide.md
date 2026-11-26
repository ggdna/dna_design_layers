<!--
@license
Copyright (c) dnaCopyrightHolder

Use of this source code is governed by terms that can be
found in the LICENSE file in the root of this package.
-->

# راهنمای لایه‌ها

## @layer سیستم لایه‌ها را بشناسید <a id="know-the-layer-system"></a>

- «لایه‌های طراحی محصول» (Layers of Product Design) کار طراحی را به هفت
  لایه در سه ناحیه تقسیم می‌کند؛ این راهنماها از
  [layers-skills](https://github.com/jamiemill/layers-skills) اثر Jamie
  Mill (MIT) پیروی می‌کنند
- لایه‌های پایین‌تر پایهٔ لایه‌های بالاترند؛ یک لایهٔ پایینِ ضعیف در هر
  لایهٔ بالاتر بدهی ایجاد می‌کند
- از هر لایه‌ای می‌توان وارد شد، اما پیش از ساختن به سمت بالا لایه‌های
  پایین‌تر را بررسی کنید

فضای مسئله — دانشی که از واقعیت گردآوری می‌شود:

- 1 [رفتار مشاهده‌شده](layers/observed-behaviour-guide.md) — کاربران
  واقعاً چه می‌کنند
- 2 [دامنه](layers/domain-guide.md) — چه چیزی پیش از محصول ما وجود دارد
- 3 [نیازهای کاربر](layers/user-needs-guide.md) — کاربران به دنبال
  رسیدن به چه چیزی هستند، و چرا

فضای راه‌حل — تصمیم‌های آگاهانه دربارهٔ آنچه ساخته می‌شود:

- 4 [راهبرد محصول](layers/product-strategy-guide.md) — کدام نیازها را
  برای کدام نتیجه پاسخ می‌دهیم
- 5 [مدل مفهومی](layers/conceptual-model-guide.md) — کدام اشیا، روابط و
  واژه‌ها
- 6 [جریان تعامل](layers/interaction-flow-guide.md) — کدام مکان‌ها،
  کنش‌ها و مسیرها
- 7 [سطح](layers/surface-guide.md) — کاربران چه می‌بینند، می‌خوانند و
  می‌شنوند

## @design طراحی را تصمیم‌گیری بدانید <a id="treat-design-as-decision-making"></a>

- هر لایه تصمیم می‌گیرد؛ مصنوعات (artefacts) فقط آن‌ها را ثبت می‌کنند
- چهار نوع پیشرفت: یک تصمیم بگیرید، تصمیمِ گرفته‌نشده‌ای را آشکار کنید،
  تصمیمی پرریسک را ارزیابی کنید، اولویت‌بندی کنید
- هر بار روی یک لایه کار کنید؛ فضای مسئله و فضای راه‌حل را مخلوط نکنید
- تصمیم‌های بد را علامت بزنید، نه فقط تصمیم‌های ناموجود را
- تصمیم‌ها را ثبت کنید، نه متن کامل گفت‌وگو؛ سابقه را کوتاه نگه دارید

## @skills از مهارت‌ها (skills) استفاده کنید <a id="use-the-skills"></a>

- `/layers-intro` را در آغاز هر جلسهٔ طراحی بارگذاری کنید
- وقتی مطمئن نیستید کدام لایه نیاز به توجه دارد، `/layers-orient` را اجرا
  کنید؛ [راهنمای جهت‌یابی](layers/orient-guide.md) را ببینید
- مهارت لایه‌ای را که روی آن کار می‌کنید اجرا کنید:
  `/layers-observed-behaviour`، `/layers-domain`، `/layers-user-needs`،
  `/layers-product-strategy`، `/layers-conceptual-model`،
  `/layers-interaction-flow`، `/layers-surface`
- هر مهارت راهنمای خود را می‌خواند؛ راهنما کتابخانه‌ای از تکنیک‌هاست، نه
  یک فیلم‌نامه: یک تکنیک برای تصمیمِ جاری برگزینید، آن را پیش ببرید و
  حاصل را ثبت کنید

## @record نتایج را ثبت کنید <a id="record-the-results"></a>

- حاصل یک جلسه را در مخزن مدیریت پروژه بنویسید؛
  [راهنمای مخزن PM](pm-repo-guide.md#use-the-design-layers) از لایهٔ
  `dna_plan` را ببینید، اگر مخزن آن را دارد
- هر تصمیم در یک فایل در `concepts/decisions`؛ هر چیز دیگر در فایل
  موضوع (topic)، UX، هدف یا نیازمندی‌ها (requirements) که به آن تعلق دارد
