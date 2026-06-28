# Task 03 — Data Faylları ilə İş

## Ssenari

> *"Pipeline konfiqurasiya faylı yaratmaq, log fayllarını analiz etmək və köhnə faylları arxivləmək lazımdır."*

---

## Tapşırıqlar

### 3.1 — Konfiqurasiya faylı yarat
`~/dataops-project/scripts/` qovluğunda `config.txt` adlı fayl yarat və aşağıdakı məzmunu əlavə et:

```
DB_HOST=localhost
DB_PORT=5432
DB_NAME=dataops
LOG_LEVEL=INFO
MAX_WORKERS=4
```

💡 **Hint:** Faylı yaratmaq üçün `touch`, məzmun əlavə etmək üçün `echo` və `>>` operatoru.

---

### 3.2 — Faylı oxu
`config.txt` faylının **tam məzmununu**, **ilk 3 sətirini** və **son 2 sətirini** ayrı-ayrı göstər.

💡 **Hint:** `cat`, `head`, `tail` əmrləri — hər biri fərqli şəkildə oxuyur.

---

### 3.3 — Log faylı yarat və axtar
`~/dataops-project/logs/` qovluğunda `pipeline.log` adlı fayl yarat və aşağıdakı məzmunu əlavə et:

```
[INFO]  2026-06-26 09:00 Pipeline started
[INFO]  2026-06-26 09:01 Reading raw data
[ERROR] 2026-06-26 09:02 Connection timeout
[INFO]  2026-06-26 09:03 Retrying...
[ERROR] 2026-06-26 09:04 File not found: sales.csv
[INFO]  2026-06-26 09:05 Pipeline finished
```

Yalnız **ERROR** sətirləri göstər. Neçə error var?

💡 **Hint:** `grep` əmri + `wc -l` — pipe `|` ilə birləşdir.

---

### 3.4 — Faylı redaktə et
`~/dataops-project/scripts/config.txt` faylında `LOG_LEVEL=INFO` dəyərini `LOG_LEVEL=DEBUG` ilə əvəz et. Faylı birbaşa dəyiş, yeni fayl yaratma.

💡 **Hint:** `sed` əmrinin faylı birbaşa dəyişən bir flag-ı var.

---

### 3.5 — Kopyala və köçür
- `config.txt` faylını `~/dataops-project/data/processed/config_backup.txt` adı ilə kopyala
- `pipeline.log` faylının adını `pipeline_2026-06-26.log` olaraq dəyiş

💡 **Hint:** Kopyalamaq üçün `cp`, adını dəyişmək/köçürmək üçün `mv`.

---

### 3.6 — Axtar
`~/dataops-project/` daxilindəki bütün `.txt` fayllarını tap.

💡 **Hint:** `find` əmri — başlanğıc qovluq və fayl adı üçün flag var.

---

## ANSWERS.md-yə nə yazmalısan?

- `cat config.txt` çıxışı (3.4-dən sonra — `LOG_LEVEL=DEBUG` görünməlidir)
- `grep "ERROR" ~/dataops-project/logs/pipeline.log` çıxışı
- Error sayı (`wc -l` nəticəsi)
- `find` çıxışı

**Bonus sual:**
`sed -i` ilə `sed` (i olmadan) fərqi nədir?
