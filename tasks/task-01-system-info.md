# Task 01 — Sistem Məlumatlarını Topla

## Ssenari

> *"Yeni serverin texniki xüsusiyyətlərini bilmək lazımdır. Aşağıdakı sualları cavablandır və nəticəni ANSWERS.md-yə yaz."*

---

## Tapşırıqlar

### 1.1 — Əməliyyat sistemi
Serverinin **OS adını, kernel versiyasını və arxitekturasını** öyrən. Bütün məlumatı bir əmrlə göstər.

💡 **Hint:** `uname` əmrinə bax — bütün məlumatı göstərən bir flag var.

---

### 1.2 — RAM vəziyyəti
Serverinin **ümumi RAM-ı, istifadə olunanı və mövcud olanı** göstər. Nəticəni **MB** olaraq göstər.

💡 **Hint:** `free` əmri var — MB üçün bir flag əlavə etmək lazımdır.

---

### 1.3 — Disk vəziyyəti
Hansı fayl sistemi ən çox **dolmuşdur**? Doluluq faizini göstər.

💡 **Hint:** `df` əmrinə bax — MB formatında göstərən flag var.

---

### 1.4 — Server neçə müddətdir işləyir?
Sistemin **işləmə müddətini** və **load average** dəyərini öyrən.

💡 **Hint:** `uptime` əmri birbaşa bu məlumatı verir.

---

### 1.5 — Hazırda kim daxil olmusan?
Hansı **istifadəçi** kimi işləyirsən? **UID** və **GID** nədir?

💡 **Hint:** İki əmr var — biri yalnız adı, digəri UID/GID məlumatını verir.

---

### 1.6 — Axırıncı işlətdiyin əmrlər
Son 15 işlətdiyin əmri listlə.

💡 **Hint:** `history` əmri var — nəticəni məhdudlaşdırmaq üçün bir rəqəm əlavə et.

---

## ANSWERS.md-yə nə yazmalısan?

Hər alt-tapşırığın terminal çıxışını `ANSWERS.md` faylındakı **Task 01** bölməsinə yapışdır.

**Bonus sual:**
`free` çıxışında `available` sütunu `free` sütunundan böyükdür — niyə?
Cavabını öz sözlərinlə bir cümlə ilə yaz.
