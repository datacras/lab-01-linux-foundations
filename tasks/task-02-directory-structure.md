# Task 02 — Layihə Qovluq Strukturunu Yarat

## Ssenari

> *"Data pipeline üçün standart qovluq strukturuna ehtiyacımız var. Aşağıdakı strukturu `home` direktoriyanda yarat:"*

```
~/dataops-project/
├── data/
│   ├── raw/
│   └── processed/
├── logs/
└── scripts/
```

---

## Tapşırıqlar

### 2.1 — Strukturu yarat
Yuxarıdakı qovluq strukturunu `home` direktoriyanda yarat.
İçiçə qovluqları **tək əmrlə** yaratmağa çalış.

💡 **Hint:** `mkdir` əmrinin içiçə qovluqları avtomatik yaradan bir flag-ı var.

---

### 2.2 — Strukturu yoxla
Yaratdığın strukturu ağac şəklində göstər.

💡 **Hint:** `tree` əmri — qurulu deyilsə əvvəlcə `apt install` et.

---

### 2.3 — Naviqasiya
`data/raw/`, `logs/` və `scripts/` qovluqlarına ardıcıl gir, hər birindən sonra **harada olduğunu** göstər.

💡 **Hint:** `cd` ilə keç, `pwd` ilə yerini yoxla.

---

### 2.4 — Relative path
`data/raw/` içindəyikən `data/processed/` qovluğuna **tam yol yazmadan** keç.

💡 **Hint:** `..` işarəsi bir üst qovluğa çıxmağa imkan verir.

---

### 2.5 — Siyahı
`dataops-project/` qovluğunun içini **gizli fayllar daxil** bütün detallarla listlə.

💡 **Hint:** `ls` əmrinin iki flag-ını birlikdə istifadə et — biri detallar, biri gizli fayllar üçün.

---

## ANSWERS.md-yə nə yazmalısan?

- `tree` çıxışı (tam struktur görünməlidir)
- Hər `cd`-dən sonrakı `pwd` çıxışı
- `ls` çıxışı

**Bonus sual:**
`mkdir` əmrinin həmin flag-ı olmadan içiçə qovluq yaratmağa çalışsan nə baş verir? Sına və yaz.
