# Task 04 — Komanda Üzvü üçün User Yarat

## Ssenari

> *"Yeni data engineer komandamıza qoşuldu: `ali`. Ona serverdə hesab açmaq, `dataops-project` qovluğunun sahibliyini vermək və icazələri düzgün qurmaq lazımdır."*

> ⚠️ **Qeyd:** Bu tapşırıq `sudo` icazəsi tələb edir.

---

## Tapşırıqlar

### 4.1 — User yarat
`ali` adlı istifadəçi yarat. Home direktoriyası avtomatik yaransın.

💡 **Hint:** `useradd` əmrinin home qovluğu yaradan bir flag-ı var.

Yarandımı yoxla — `/etc/passwd` faylında `ali`-ni axtar.

💡 **Hint:** `cat` + `grep` ilə.

---

### 4.2 — Şifrə təyin et
`ali` üçün şifrə təyin et: `DataCras2026!`

💡 **Hint:** `passwd` əmri — hansı user üçün olduğunu da bildirmək lazımdır.

---

### 4.3 — Sahibliyi ver
`~/dataops-project/` qovluğunun sahibini `ali` olaraq dəyiş. Qovluğun içindəkilərə də tətbiq olsun.

💡 **Hint:** `chown` əmrinin rekursiv işləyən bir flag-ı var.

Dəyişdi mi? `ls -la ~` ilə yoxla.

---

### 4.4 — `config.txt` icazələrini qur
`~/dataops-project/scripts/config.txt` faylı üçün:
- **Sahibi** oxuyub yaza bilsin
- **Qrup və digərləri** yalnız oxusun

💡 **Hint:** `chmod` — rəqəmsal (octal) format istifadə et.

---

### 4.5 — `logs/` qovluğunu qoru
`~/dataops-project/logs/` qovluğuna **yalnız sahibi** girə bilsin, başqaları heç bir icazəyə malik olmasın.

💡 **Hint:** `chmod` — tam bağlı qovluq üçün hansı rəqəm lazımdır?

---

### 4.6 — `ls -l` çıxışını oxu
`config.txt` faylına `ls -l` işlət. Çıxışdakı hər sütunu izah et:
- Fayl tipi nədir?
- Owner və Group kim?
- `rw-r--r--` nə deməkdir?

---

## ANSWERS.md-yə nə yazmalısan?

- `cat /etc/passwd | grep ali` çıxışı
- `ls -la ~` çıxışı (chown-dan sonra — sahibin `ali` olduğu görünməlidir)
- `ls -l config.txt` çıxışı (chmod-dan sonra)
- `ls -ld logs/` çıxışı
- 4.6-nın izahı (öz sözlərinlə)

**Bonus sual:**
`chmod 644` əvəzinə symbolic olaraq necə yazardın? (`u`, `g`, `o` ilə)
