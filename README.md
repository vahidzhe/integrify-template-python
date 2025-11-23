# Integrify Template

Bu reponu istifadə etməklə yeni inteqrasiyaları yaradıb, ekosistemə uyğun alt-kitabaxanalar yaratmaq asanlaşır.

## Addımlar

### 1. Repository yaradın
Sağ yuxarı küncdə **"Use this template → Create new repository"** seçin.

### 2. Lokalınıza yükləyin
```bash
git clone git clone git@github.com:Integrify-SDK/integrify-{integration_name}-python.git
cd integrify-{integration_name}-python
```

### 3. Lokal konfiqurasiya yaradın
```bash
python create_local_configs.py
```

### 4. İnteqrasiya adını dəyişdirin
`integration_name` qovluğunu işləyəcəyiniz inteqrasiyanın adına dəyişin.

### 5. Placeholder-ləri əvəz edin
- Ümumi axtarış açın (Ctrl+Shift+F)
- `{replace}` string-ini axtarın
- Həmin yerləri inteqrasiyanın adı ilə yeniləyin

### 6. Alətləri quraşdırın

#### 📦 `uv` quraşdırılması
`uv` Python paket meneceridir. Quraşdırmaq üçün:

> [!NOTE]
> Ətraflı məlumat üçün: https://docs.astral.sh/uv/getting-started/installation/

<details>
<summary><strong>Windows</strong></summary>

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```
</details>

<details>
<summary><strong>macOS/Linux</strong></summary>

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
</details>

#### 🔨 `make` quraşdırılması
`make` build avtomatlaşdırma alətidir.

<details>
<summary><strong>Windows (Chocolatey ilə)</strong></summary>

Əvvəlcə Chocolatey yoxlanılmalıdır:
```powershell
choco --version
```

Əgər Chocolatey quraşdırılmayıbsa:

> [!IMPORTANT]
> Administrator PowerShell açın və aşağıdakı əmri icra edin:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Ətraflı məlumat: https://chocolatey.org/install

Chocolatey quraşdırıldıqdan sonra `make` yükləyin:
```powershell
choco install make
```
</details>

<details>
<summary><strong>macOS</strong></summary>

```bash
brew install make
```
</details>

<details>
<summary><strong>Linux</strong></summary>

```bash
# Ubuntu/Debian
sudo apt install make

# CentOS/RHEL
sudo yum install make
```
</details>

### 7. Paketləri quraşdırın və başlayın
```bash
uv sync
pre-commit install
```

İndi `make` əmrlərindən istifadə edə bilərsiniz:
```bash
make help  # Mövcud əmrləri görmək üçün
```

## Əlavə məlumat

- `pre-commit` hook-ları kodu commit etməzdən əvvəl yoxlayır
- `uv` sürətli və müasir Python paket meneceridir
- `make` kommandları proyekt üçün tez-tez istifadə olunan əmrləri sadələşdirir