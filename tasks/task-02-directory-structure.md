# Task 02 — Layihə Qovluq Strukturunu Yarat

## Ssenari

> *"Data pipeline üçün standart qovluq strukturuna ehtiyacımız var. Aşağıdakı strukturu `home` direktoriyanda yarat:"*

```
~/dataops-project/
├── data/
│   ├── raw/
│   └── processed/
├── logs/
└── scripts/
```

---

## Tapşırıqlar

### 2.1 — Strukturu bir əmrlə yarat

```bash
mkdir -p ~/dataops-project/data/raw \
          ~/dataops-project/data/processed \
          ~/dataops-project/logs \
          ~/dataops-project/scripts
```

### 2.2 — Strukturu yoxla

`tree` əmri ilə yarat strukturu göstər:

```bash
tree ~/dataops-project
```

> `tree` qurulu deyilsə: `sudo apt install -y tree`

### 2.3 — Hər qovluğa cd ilə gir, pwd ilə yerini yoxla

```bash
cd ~/dataops-project/data/raw
pwd

cd ~/dataops-project/logs
pwd

cd ~
pwd
```

### 2.4 — Relative path ilə naviqasiya

`~/dataops-project/data/raw` içindəyikən `processed` qovluğuna **relative path** ilə keç:

```bash
cd ~/dataops-project/data/raw
cd ../processed
pwd
```

### 2.5 — Qovluqların siyahısı

`dataops-project` içindən `ls -la` ilə bütün qovluqları listlə:

```bash
ls -la ~/dataops-project/
```

---

## ANSWERS.md-yə nə yazmalısan?

- `tree ~/dataops-project` çıxışı
- `pwd` çıxışları (hər cd-dən sonra)
- `ls -la` çıxışı

**Bonus sual:**
`mkdir -p` olmadan `mkdir ~/dataops-project/data/raw` işləyərmi? Niyə?
