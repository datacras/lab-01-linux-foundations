# Task 05 — Proses Monitorinqi

## Ssenari

> *"Server bu gün bir az yavaş görünür. Nə baş verdiyini araşdır. Background-da işləyən prosesləri tap və resurs istifadəsinə bax."*

---

## Tapşırıqlar

### 5.1 — Bütün prosesləri listlə

```bash
ps aux
```

Çıxışda bu sualları cavablandır:
- Ən yuxarıdakı proses nədir? (PID 1)
- `bash` prosesi işləyirmi?
- Neçə proses var cəmi?

```bash
ps aux | wc -l
```

### 5.2 — Background proseslər başlat

```bash
sleep 300 &
sleep 400 &
sleep 500 &
```

Job-ları gör:

```bash
jobs
```

### 5.3 — ps ilə tap

```bash
ps aux | grep sleep
```

`grep sleep` prosesinin özü də çıxışda görünür — niyə? Onu filterlə:

```bash
ps aux | grep sleep | grep -v grep
```

### 5.4 — PID-ləri öyrən

```bash
pgrep sleep
```

Neçə `sleep` prosesi işləyir?

```bash
pgrep sleep | wc -l
```

### 5.5 — Birini dayandır

Birinci `sleep` prosesinin PID-ini götür və **SIGTERM** ilə dayandır:

```bash
kill $(pgrep sleep | head -1)
jobs
```

### 5.6 — Qalanları məcburi dayandır

```bash
kill -9 $(pgrep sleep)
jobs
```

Hamısı getdimi?

### 5.7 — Sistem resurs vəziyyəti

```bash
uptime
```

Load average nədir? Normal sayılırmı?

---

## ANSWERS.md-yə nə yazmalısan?

- `ps aux | wc -l` nəticəsi
- `jobs` çıxışı (3 sleep başlatdıqdan sonra)
- `ps aux | grep sleep | grep -v grep` çıxışı
- `pgrep sleep | wc -l` nəticəsi
- `kill` əmrlərindən sonra `jobs` çıxışı
- `uptime` çıxışı

**Bonus sual:**
`kill` ilə `kill -9` fərqi nədir? Nə vaxt hansını işlətmək lazımdır?
