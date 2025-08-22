<div dir=rtl>

# يـوتلب Utilib

[[English]](readme.md)

مجموعة من المساعدات المتنوعة للغة الأسس البرمجية.

---

## مساعدات متنوعة

### محارف_أو_قيمة_مبدئية (charsPtrOrDefault)

```
ماكرو محارف_أو_قيمة_مبدئية [القيمة، الافتراضية]
```

<div dir=ltr>

```
macro charsPtrOrDefault [val, default]
```

</div>

تعيد القيمة المعطاة، أو القيمة الافتراضية إذا كانت القيمة المعطاة تساوي 0.

### متغير_محيطي_أو_قيمة_مبدئية (envVarOrDefault)

```
ماكرو متغير_محيطي_أو_قيمة_مبدئية [اسم_المتغير، القيمة_الافتراضية] 
```

<div dir=ltr>

```
macro envVarOrDefault [varName, defaultVal]
```

</div>

تستخرج قيمة متغيّر بيئي، أو تعيد قيمة افتراضية إذا لم يكن المتغيّر البيئي معرفًا.

---

## مساعدات إنشاء عناصر ش.ب.م (AST)

تُدرج هذه الماكروهات عقد AST في وقت المعالجة التمهيدية عبر `نـبم.مدير_شبم` (`Spp.astMgr`).

### سلسلة_محارف_من_قيمة (strLiteralFromVal)

```
ماكرو سلسلة_محارف_من_قيمة [القيمة] 
```

<div dir=ltr>

```
macro strLiteralFromVal [val]
```

</div>

يُدرج عقدة AST لعنصر نصي (string literal) من قيمة (مؤشر محارف) معطاة.

```
ماكرو سلسلة_محارف_من_قيمة [القيمة، الافتراضية] 
```

<div dir=ltr>

```
macro strLiteralFromVal [val, default]
```

</div>

مثل النسخة السابقة، ولكن ترجع قيمة افتراضية إذا كانت القيمة المعطاة 0.

### سلسلة_محارف_من_متغير_محيطي (strLiteralFromEnvVar)

```
ماكرو سلسلة_محارف_من_متغير_محيطي [اسم_المتغير]
```

<div dir=ltr>

```
macro strLiteralFromEnvVar [varName]
```

</div>

اختصار لإنشاء عنصر نصي من متغيّر بيئي. يجب أن يكون المتغيّر معرفًا.

```
ماكرو سلسلة_محارف_من_متغير_محيطي [اسم_المتغير، القيمة_الافتراضية]
```

<div dir=ltr>

```
macro strLiteralFromEnvVar [varName, default]
```

</div>

مثل السابق لكن مع قيمة افتراضية.

### صحيح_حرفي_من_صحيح (intLiteralFromInt)

```
ماكرو صحيح_حرفي_من_صحيح [القيمة]
```

<div dir=ltr>

```
macro intLiteralFromInt [val]
```

</div>

يُدرج عقدة AST لعنصر عدد صحيح (integer literal) من قيمة رقمية معطاة.

### صحيح_حرفي_من_محارف (intLiteralFromCharsPtr)

```
ماكرو صحيح_حرفي_من_محارف [القيمة]
```

<div dir=ltr>

```
macro intLiteralFromCharsPtr [val]
```

</div>

يُدرج عقدة AST لعنصر عدد صحيح من سلسلة محارف (`CharsPtr`). يجب أن تحتوي السلسلة على رقم.

```
ماكرو صحيح_حرفي_من_محارف [القيمة، الافتراضية]
```

<div dir=ltr>

```
macro intLiteralFromCharsPtr [val, default]
```

</div>

مثل السابق مع قيمة افتراضية إذا كانت القيمة المعطاة فارغة (0).

### صحيح_حرفي_من_متغير_محيطي (intLiteralFromEnvVar)

```
ماكرو صحيح_حرفي_من_متغير_محيطي [اسم_المتغير]
```

<div dir=ltr>

```
macro intLiteralFromEnvVar [varName]
```

</div>

ينشئ عقدة AST لعنصر عدد صحيح من متغيّر بيئي نصي. يجب أن يكون المتغيّر معرّفًا ويجب أن يحتوي على رقم.

```
ماكرو صحيح_حرفي_من_متغير_محيطي [اسم_المتغير، القيمة_الافتراضية]
```

<div dir=ltr>

```
macro intLiteralFromEnvVar [varName, default]
```

</div>

مثل السابق مع قيمة افتراضية.

---

## مساعدات الوقت والتاريخ

### هات_التاريخ_والوقت_الحالي_كنص (getCurrentStringDateTime)

```
دالة هات_التاريخ_والوقت_الحالي_كنص () => نـص
```

<div dir=ltr>

```
function getCurrentStringDateTime() => String
```

</div>

تعيد التاريخ والوقت الحالي للنظام كسلسلة محارف منسّقة.

**الإرجاع**

سلسلة محارف بصيغة: `YYYY-MM-DD HH:MM:SS`

```
دالة هات_التاريخ_والوقت_الحالي_كنص () => نـص
```

<div dir=ltr>

```
function getCurrentStringDateTime(timestamp: ArchInt) => String
```

</div>

تعيد التاريخ والوقت المقابل للختم الزمني المعطى (`timestamp`) كسلسلة محارف منسّقة.

**الإرجاع**

سلسلة محارف بصيغة: `YYYY-MM-DD HH:MM:SS`

</div>

