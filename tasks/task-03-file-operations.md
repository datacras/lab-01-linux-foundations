# Task 03 — Data Faylları ilə İş

## Ssenari

> *"Pipeline konfiqurasiya faylı yaratmaq, log fayllarını analiz etmək və köhnə faylları arxivləmək lazımdır."*

---

## Tapşırıqlar

### 3.1 — Konfiqurasiya faylı yarat

`scripts/` qovluğunda `config.txt` faylı yarat və məzmun əlavə et:

```bash
cd ~/dataops-project/scripts

touch config.txt

echo "DB_HOST=localhost" >> config.txt
echo "DB_PORT=5432" >> config.txt
echo "DB_NAME=dataops" >> config.txt
echo "LOG_LEVEL=INFO" >> config.txt
echo "MAX_WORKERS=4" >> config.txt
```

### 3.2 — Faylı oxu

```bash
cat config.txt
head -3 config.txt
tail -2 config.txt
```

### 3.3 — Log faylı yarat və axtar

`logs/` qovluğunda `pipeline.log` faylı yarat:

```bash
cd ~/dataops-project/logs

echo "[INFO]  2026-06-26 09:00 Pipeline started" >> pipeline.log
echo "[INFO]  2026-06-26 09:01 Reading raw data" >> pipeline.log
echo "[ERROR] 2026-06-26 09:02 Connection timeout" >> pipeline.log
echo "[INFO]  2026-06-26 09:03 Retrying..." >> pipeline.log
echo "[ERROR] 2026-06-26 09:04 File not found: sales.csv" >> pipeline.log
echo "[INFO]  2026-06-26 09:05 Pipeline finished" >> pipeline.log
```

**Yalnız ERROR sətirləri tapın:**

```bash
grep "ERROR" pipeline.log
```

**Neçə error var?**

```bash
grep "ERROR" pipeline.log | wc -l
```

### 3.4 — sed ilə dəyiş

`config.txt` faylında `LOG_LEVEL=INFO` dəyərini `LOG_LEVEL=DEBUG` ilə əvəz et:

```bash
cd ~/dataops-project/scripts
sed -i 's/LOG_LEVEL=INFO/LOG_LEVEL=DEBUG/' config.txt
cat config.txt
```

### 3.5 — Faylı kopyala və köçür

```bash
# Konfig faylını data/processed/ qovluğuna kopyala
cp config.txt ~/dataops-project/data/processed/config_backup.txt

# Yoxla
ls -l ~/dataops-project/data/processed/

# Log faylını arxivlə (köçür)
mv ~/dataops-project/logs/pipeline.log \
   ~/dataops-project/logs/pipeline_2026-06-26.log

ls ~/dataops-project/logs/
```

### 3.6 — find ilə axtar

`dataops-project` içindəki bütün `.txt` fayllarını tap:

```bash
find ~/dataops-project -name "*.txt"
```

---

## ANSWERS.md-yə nə yazmalısan?

- `cat config.txt` çıxışı (sed-dən sonra)
- `grep "ERROR" pipeline.log` çıxışı
- `grep "ERROR" pipeline.log | wc -l` nəticəsi
- `find` çıxışı

**Bonus sual:**
`sed -i` ilə `sed` (i olmadan) fərqi nədir?
