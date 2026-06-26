# Task 04 — Komanda Üzvü üçün User Yarat

## Ssenari

> *"Yeni data engineer komandamıza qoşuldu: `ali`. Ona serverdə hesab açmaq və `dataops-project` qovluğuna çıxış vermək lazımdır."*

> ⚠️ **Qeyd:** Bu tapşırıq `sudo` icazəsi tələb edir. `root` kimi və ya `sudo` ilə işlə.

---

## Tapşırıqlar

### 4.1 — Yeni user yarat

```bash
sudo useradd -m ali
```

User yarandımı? Yoxla:

```bash
cat /etc/passwd | grep ali
```

### 4.2 — Şifrə təyin et

```bash
sudo passwd ali
# Şifrə: DataCras2026!
# (iki dəfə yaz)
```

### 4.3 — `dataops-project` üçün icazələri yoxla

`dataops-project` qovluğunun hazırki sahibini və icazələrini gör:

```bash
ls -la ~ | grep dataops-project
```

Çıxışı oxu:
- Sahibi kim?
- İcazə sətri nədir? (`drwxr-xr-x` kimi)
- `ali` bu qovluğu oxuya bilərmi? Niyə?

### 4.4 — `scripts/config.txt` faylının icazələrini dəyiş

`config.txt` faylını **sahibi** oxuyub yaza bilsin, **qrup və digərləri** yalnız oxusun:

```bash
chmod 644 ~/dataops-project/scripts/config.txt
ls -l ~/dataops-project/scripts/config.txt
```

### 4.5 — `logs/` qovluğuna yalnız sahibi girə bilsin

```bash
chmod 700 ~/dataops-project/logs/
ls -ld ~/dataops-project/logs/
```

### 4.6 — `ls -l` çıxışını oxu

```bash
ls -l ~/dataops-project/scripts/config.txt
```

Çıxışı `ANSWERS.md`-yə yapışdır və hər sütunu izah et:
- Fayl tipi nədir? (`-` nə deməkdir?)
- Owner kim?
- Group kim?
- `rw-r--r--` icazəsi nə deməkdir?

---

## ANSWERS.md-yə nə yazmalısan?

- `cat /etc/passwd | grep ali` çıxışı
- `ls -l config.txt` çıxışı (chmod-dan sonra)
- `ls -ld logs/` çıxışı
- 4.6-nın izahı (öz sözlərinlə)

**Bonus sual:**
`chmod 644` əvəzinə symbolic olaraq necə yazardın? (`u=`, `g=`, `o=` ilə)
