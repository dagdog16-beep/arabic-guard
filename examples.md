# Examples — broken Arabic vs Arabic Guard output

Real breakage patterns, and the corrected form the skill produces.

## 1. Reversed text (the classic PDF/Word extraction break)

Broken (characters reversed):
```
ءاثالثلا موي ةروتافلا ينتلصو
```
Correct:
```
وصلتني الفاتورة يوم الثلاثاء
```

## 2. Price stranded at the wrong edge

Broken:
```
دولار يوم الثلاثاء 500 دفعت
```
Correct:
```
دفعت 500 دولار يوم الثلاثاء
```

## 3. Latin fragment swallowing the sentence

Broken:
```
سأرسل لك le rapport غداً إن شاء الله
```
Correct (natural Arabic, established term kept only if needed):
```
سأرسل لك التقرير غداً إن شاء الله
```

## 4. Punctuation at the wrong end

Broken:
```
؟هل وصلتك الرسالة
```
Correct:
```
هل وصلتك الرسالة؟
```

## 5. A file that opens the wrong way

Broken HTML:
```html
<p>مرحبا بكم في متجرنا</p>
```
Correct HTML:
```html
<p dir="rtl" lang="ar">مرحبا بكم في متجرنا</p>
```

## 6. Digits mixed between two systems

Broken:
```
المجموع ١٢٥٠ دولار و 300 سنت
```
Correct (one system, matching the reader's convention):
```
المجموع 1250 دولار و300 سنت
```
