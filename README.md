# 🧪 Lab 01 — Linux Foundations

## Ssenari

Siz **DataCras** şirkətinin Data Engineering komandasına yeni qoşuldunuz.
Komanda lideriniz ilk iş günündə sizə bir Ubuntu serveri verib və aşağıdakı tapşırıqları göndərib:

> *"Serveri data pipeline işi üçün hazırlamaq lazımdır. Aşağıdakı tapşırıqları ardıcıl olaraq tamamla və hər birinin nəticəsini `ANSWERS.md` faylında qeyd et. Uğurlar! 🚀"*
>
> — *Komanda lideri*

---

## Tapşırıqlar

| # | Tapşırıq | Mövzu |
|---|---|---|
| [Task 01](tasks/task-01-system-info.md) | Sistem məlumatlarını topla | `uname`, `free`, `df`, `uptime`, `history` |
| [Task 02](tasks/task-02-directory-structure.md) | Layihə qovluq strukturunu yarat | `mkdir`, `tree`, `pwd` |
| [Task 03](tasks/task-03-file-operations.md) | Data faylları ilə iş | `cat`, `echo`, `grep`, `sed`, `cp`, `mv`, `find` |
| [Task 04](tasks/task-04-user-management.md) | Komanda üzvü üçün user yarat | `useradd`, `chmod`, `chown`, `ls -l` |
| [Task 05](tasks/task-05-process-monitoring.md) | Proses monitorinqi | `ps`, `pgrep`, `kill`, `jobs` |
| [Task 06](tasks/task-06-package-management.md) | Lazımi alətləri quraşdır | `apt install`, `apt show`, `apt remove` |

---

## Necə submit edəcəksən?

1. Bu repo-nu **fork** et — sağ yuxarıdakı "Fork" düyməsinə bas
2. Fork-ladığın repo-nu Ubuntu serverinə clone et:
   ```bash
   git clone https://github.com/SƏNIN-USERNAME/lab-01-linux-foundations.git
   cd lab-01-linux-foundations
   ```
3. Tapşırıqları et, nəticələri `ANSWERS.md`-yə yapışdır
4. Push et:
   ```bash
   git add ANSWERS.md
   git commit -m "Lab 01 tamamlandı"
   git push
   ```

> 🐙 **Git ilk dəfəmi?** → [GIT-GUIDE.md](GIT-GUIDE.md) — fork, clone, push addım-addım izah edilib

---

## Qiymətləndirmə

| Meyar | Bal |
|---|---|
| Hər task tamamlanıb | 6 × 10 = 60 |
| Çıxışlar doğru və oxunaqlıdır | 20 |
| Commit mesajı yazılıb | 10 |
| Vaxtında təhvil | 10 |
| **Cəmi** | **100** |

---

> 💡 **Sıxışdığında:** Presentation materiallarına bax → [datacras.github.io/dpe-01-linux](https://datacras.github.io/dpe-01-linux)
