# Task 01 — Sistem Məlumatlarını Topla

## Ssenari

Komanda lideriniz sizə bu mesajı göndərdi:

> *"Yeni serverin texniki xüsusiyyətlərini bilmək lazımdır. Aşağıdakı sualları cavablandır və nəticəni ANSWERS.md-yə yaz."*

---

## Tapşırıqlar

### 1.1 — Əməliyyat sistemi
Serverinin **OS adını, kernel versiyasını və arxitekturasını** öyrən.

```bash
uname -a
```

### 1.2 — RAM vəziyyəti
Serverinin **ümumi RAM-ı, istifadə olunanı və mövcud olanı** MB olaraq göstər.

```bash
free -m
```

### 1.3 — Disk vəziyyəti
Hansı **fayl sistemi** ən çox dolmuşdur? Faiz olaraq göstər.

```bash
df -m
```

### 1.4 — Server neçə müddətdir işləyir?
`uptime` əmri ilə **sistem işləmə müddətini** və **load average-i** öyrən.

```bash
uptime
```

### 1.5 — Sən kimin adındasın?
Hazırda hansı **istifadəçi** kimi daxil olmusan? UID-in nədir?

```bash
whoami
id
```

---

## ANSWERS.md-yə nə yazmalısan?

Her əmrin **çıxışını** kopyalayıb `ANSWERS.md` faylındakı Task 01 bölməsinə yapışdır.

**Bonus sual (məcburi deyil):**
`free -m` çıxışında `available` sütunu `free` sütunundan böyükdür — niyə?
Cavabını öz sözlərinlə bir cümlə ilə yaz.
