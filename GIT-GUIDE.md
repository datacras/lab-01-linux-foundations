# 🐙 Git Bələdçisi — İlk Dəfə İstifadəçilər üçün

> Bu sənəd Lab 01-i submit etmək üçün lazım olan bütün Git addımlarını izah edir.
> Git dərslərindən əvvəl bu bələdçi ilə ilk təcrübəni qazanacaqsan.

---

## Git nədir?

**Git** — kod və faylların dəyişiklik tarixçəsini izləyən versiya idarəetmə sistemidir.
**GitHub** — Git repo-larını internetdə saxlayan platformadır.

```
Sənin Ubuntu serverin  →  git push  →  GitHub
GitHub                 →  git pull  →  Sənin Ubuntu serverin
```

---

## Addım 1 — GitHub Hesabı Aç

1. `github.com` → **Sign up**
2. Username, email, şifrə daxil et
3. Hesabı təsdiqlə (email gələcək)

> **Username seçimi:** Ad.Soyad və ya adın kiçik hərflə — məs: `ali.mammadov`

---

## Addım 2 — Repo-nu Fork et

"Fork" — bu repo-nun surətini **öz GitHub hesabına** köçürmək deməkdir.

1. `github.com/datacras/lab-01-linux-foundations` linkini aç
2. Sağ yuxarıdakı **"Fork"** düyməsinə bas
3. **"Create fork"** — öz hesabında eyni adlı repo yaranır

İndi sənin repo-nun ünvanı belədir:
```
github.com/SƏNIN-USERNAME/lab-01-linux-foundations
```

---

## Addım 3 — Ubuntu Serverinə Git Qur

```bash
sudo apt update
sudo apt install -y git
git --version
```

---

## Addım 4 — Git Konfiqurasiyası

Git-ə adını və emailini tanıt (bir dəfə edilir):

```bash
git config --global user.name "Ad Soyad"
git config --global user.email "email@example.com"

# Yoxla
git config --list
```

---

## Addım 5 — Repo-nu Serverə Clone et

"Clone" — GitHub-dakı repo-nu Ubuntu serverinə endirmək deməkdir.

```bash
# SƏNIN-USERNAME-i öz GitHub username-inlə əvəz et
git clone https://github.com/SƏNIN-USERNAME/lab-01-linux-foundations.git

# Qovluğa gir
cd lab-01-linux-foundations

# Faylları gör
ls -l
```

Belə bir çıxış görəcəksən:
```
ANSWERS.md
GIT-GUIDE.md
README.md
tasks/
```

---

## Addım 6 — Lab Tapşırıqlarını et

`tasks/` qovluğundakı tapşırıqları oxu, Ubuntu serverindən əmrləri işlət və nəticələri `ANSWERS.md` faylına yapışdır:

```bash
# ANSWERS.md faylını nano ilə aç
nano ANSWERS.md

# Müvafiq bölməyə terminal çıxışını yapışdır
# Yadda saxla: Ctrl+O → Enter → Ctrl+X
```

---

## Addım 7 — Dəyişiklikləri GitHub-a göndər

Tapşırıqları bitirdikdən sonra bu 3 əmri işlət:

```bash
# 1. Hansı fayllar dəyişdi? — yoxla
git status

# 2. ANSWERS.md-ni hazırla (stage et)
git add ANSWERS.md

# 3. Dəyişikliyi qeyd et (commit et)
git commit -m "Lab 01 ANSWERS.md tamamlandı"

# 4. GitHub-a göndər (push et)
git push
```

GitHub username və şifrəni soruşacaq — daxil et.

> **Qeyd:** Şifrə əvəzinə GitHub **Personal Access Token** lazım ola bilər.
> `github.com` → Settings → Developer settings → Personal access tokens → Generate new token (classic) → `repo` seçimini işarələ → kopyala → şifrə yerinə yapışdır.

---

## Addım 8 — Submit-i yoxla

1. `github.com/SƏNIN-USERNAME/lab-01-linux-foundations` linkini aç
2. `ANSWERS.md` faylını gör — dəyişikliklərin orada olmalıdır
3. Sağ yuxarıda son commit tarixi görünür

---

## Xülasə — 4 Əsas Əmr

```bash
git status        # nə dəyişdi?
git add FILE      # faylı hazırla
git commit -m ""  # dəyişikliyi qeyd et
git push          # GitHub-a göndər
```

---

## Kömək lazımdırsa

- Presentation materialları: [datacras.github.io/dpe-01-linux](https://datacras.github.io/dpe-01-linux)
- `git status` çıxışını müəllimə göndər — problemi birlikdə həll edərik
