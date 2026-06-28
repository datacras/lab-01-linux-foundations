# Task 06 — Lazımi Alətləri Quraşdır

## Ssenari

> *"Data pipeline işi üçün serverə bir neçə alət lazımdır: `git` (kod versiyalanması), `curl` (API sorğuları), `tree` (qovluq strukturu) və `htop` (monitoring). Bunları quraşdır, yoxla və lazım olmayanı sil."*

---

## Tapşırıqlar

### 6.1 — Repository siyahısını yenilə
Paket quraşdırmadan əvvəl **həmişə** repository siyahısını yenilə. Neçə paket yenilənə bilər?

💡 **Hint:** `apt update` — yenilənə bilənlər üçün başqa bir `apt list` flag-ı var.

---

### 6.2 — Alətləri quraşdır
`git`, `curl`, `tree` və `htop` paketlərini **tək əmrlə**, sual soruşmadan quraşdır.

💡 **Hint:** `apt install` — bir neçə paketi boşluqla ayırıb yaz. Sual soruşmamaq üçün flag var.

---

### 6.3 — Qurulduğunu yoxla
Hər alət üçün **versiyasını** və ya **harada olduğunu** göstər.

💡 **Hint:** `--version` flag-ı və ya `which` əmri.

---

### 6.4 — Paket haqqında məlumat al
`curl` paketi haqqında ətraflı məlumat al. Bu məlumatdan tap:
- Versiyası nədir?
- Disk ölçüsü nə qədərdir?
- Hansı paketlərə dependency var?

💡 **Hint:** `apt show` əmri.

---

### 6.5 — Qurulu paketlər siyahısı
Sistemdə neçə paket qurulmuşdur? `git` qurulu paketlər arasındamı?

💡 **Hint:** `apt list --installed` — `grep` ilə filtrə et, `wc -l` ilə say.

---

### 6.6 — `htop`-u işlət
`htop`-u işlət, ekranda gördüklərini 2 cümlə ilə `ANSWERS.md`-yə yaz. Çıxmaq üçün `q`.

---

### 6.7 — `htop`-u sil
`htop` artıq lazım deyil — sil. Silindikdən sonra yoxla.

💡 **Hint:** `apt remove` — silindikdən sonra `which htop` ilə yoxla.

---

### 6.8 — Təmizlik
Artıq lazımsız qalan dependency paketlərini sil.

💡 **Hint:** `apt autoremove`.

---

## ANSWERS.md-yə nə yazmalısan?

- `git --version` və `curl --version` çıxışı
- `apt show curl` → Version + Depends sətirləri
- `apt list --installed | wc -l` nəticəsi
- `htop` haqqında 2 cümlə izah
- `which htop` çıxışı (silindikdən sonra)

**Bonus sual:**
`apt remove` ilə `apt purge` fərqi nədir? Hansını nə vaxt işlətmək lazımdır?
