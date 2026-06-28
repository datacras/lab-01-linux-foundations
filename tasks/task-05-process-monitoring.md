# Task 05 — Proses Monitorinqi

## Ssenari

> *"Server bu gün bir az yavaş görünür. Nə baş verdiyini araşdır. Background-da işləyən prosesləri tap və lazım olmayanları dayandır."*

---

## Tapşırıqlar

### 5.1 — Bütün prosesləri listlə
Sistemdəki **bütün** prosesləri göstər. Cəmi neçə proses var?

💡 **Hint:** `ps` əmrinin bütün prosesləri göstərən flag kombinasiyası var. Sonra `wc -l` ilə say.

Çıxışda bu sualları cavablandır:
- PID 1 hansı prosesdir?
- `bash` prosesi işləyirmi?

---

### 5.2 — Background proseslər başlat
3 ədəd `sleep` prosesi **background-da** başlat (300, 400, 500 saniyəlik).
Aktiv job-ları listlə.

💡 **Hint:** Əmrin sonuna `&` əlavə etmək onu background-a göndərir. `jobs` ilə yoxla.

---

### 5.3 — Prosesləri tap
`sleep` proseslərini **yalnız** `ps` ilə tap. Nəticədə `grep` prosesinin özü də görünürsə onu filtr et.

💡 **Hint:** `ps` + `grep` — `grep`-in özünü nəticədən çıxarmaq üçün `grep -v` istifadə et.

---

### 5.4 — PID-ləri öyrən
`sleep` proseslərinin PID-lərini tap. Neçə ədəd var?

💡 **Hint:** `pgrep` əmri birbaşa PID qaytarır. `wc -l` ilə say.

---

### 5.5 — Birini nəzakətlə dayandır
`sleep` proseslərindən **birincisini** SIGTERM ilə dayandır. Job siyahısına bax.

💡 **Hint:** `kill` + PID. İlk PID-i tapmaq üçün `pgrep` + `head -1` birləşdir.

---

### 5.6 — Qalanlarını məcburi dayandır
Qalan `sleep` proseslərini **məcburi** dayandır.

💡 **Hint:** `kill -9` — bütün PID-ləri eyni anda vermək üçün `pgrep` ilə birləşdir.

Job siyahısına bax — hamısı getdimi?

---

### 5.7 — Sistem yükünü yoxla
Sistemin **neçə müddətdir** işlədiyini və **load average**-i göstər.

💡 **Hint:** `uptime` — load average-in 3 rəqəmi nə deməkdir?

---

## ANSWERS.md-yə nə yazmalısan?

- `ps` + `wc -l` nəticəsi (PID 1 və bash haqqında şərhlə)
- `jobs` çıxışı (3 sleep-dən sonra)
- `ps | grep sleep | grep -v grep` çıxışı
- `pgrep sleep | wc -l` nəticəsi
- `jobs` çıxışı (bütün kill-lərdən sonra)
- `uptime` çıxışı

**Bonus sual:**
`kill` ilə `kill -9` fərqi nədir? Nə vaxt hansını işlətmək lazımdır?
