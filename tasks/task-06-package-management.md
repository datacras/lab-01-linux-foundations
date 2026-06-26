# Task 06 — Lazımi Alətləri Quraşdır

## Ssenari

> *"Data pipeline işi üçün serverə bir neçə alət lazımdır: `git` (kod versiyalanması), `curl` (API sorğuları), `tree` (qovluq strukturu) və `htop` (monitoring). Bunları quraşdır, yoxla və lazım olmayanı sil."*

---

## Tapşırıqlar

### 6.1 — Repository yenilə (HƏMİŞƏ İLK ADDIM)

```bash
sudo apt update
```

Neçə paket yenilənə bilər?

```bash
apt list --upgradeable 2>/dev/null | wc -l
```

### 6.2 — Alətləri quraşdır

```bash
sudo apt install -y git curl tree htop
```

### 6.3 — Qurulduğunu yoxla

```bash
git --version
curl --version | head -1
which tree
which htop
```

### 6.4 — Paket məlumatına bax

`curl` haqqında ətraflı məlumat al:

```bash
apt show curl
```

Bu məlumatdan tap:
- Versiyası nədir?
- Ölçüsü nə qədərdir?
- Hansı paketlərə dependency var?

### 6.5 — Qurulu paketlər siyahısı

Sistemdə neçə paket qurulmuşdur?

```bash
apt list --installed 2>/dev/null | wc -l
```

`git` qurulu paketlər arasındamı?

```bash
apt list --installed 2>/dev/null | grep git
```

### 6.6 — `htop`-u işlət və çıx

```bash
htop
```

`htop` ekranında gördüklərini 2 cümlə ilə `ANSWERS.md`-yə yaz.
Çıxmaq üçün: `q`

### 6.7 — `htop`-u sil

```bash
sudo apt remove htop
```

Silindi mi?

```bash
which htop
htop
```

### 6.8 — Lazımsız paketləri təmizlə

```bash
sudo apt autoremove -y
```

---

## ANSWERS.md-yə nə yazmalısan?

- `git --version` və `curl --version` çıxışı
- `apt show curl` → Version + Depends sətirləri
- `apt list --installed | wc -l` nəticəsi
- `htop` haqqında 2 cümlə izah
- `which htop` çıxışı (silindikdən sonra)

**Bonus sual:**
`apt remove htop` ilə `apt purge htop` fərqi nədir? Hansını nə vaxt işlətmək lazımdır?
