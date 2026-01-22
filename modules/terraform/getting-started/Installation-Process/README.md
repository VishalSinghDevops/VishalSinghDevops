# Terraform Installation Guide
---

## 1. Install Terraform on Ubuntu / Debian

### Method 1: Install using HashiCorp APT Repository (Recommended)

```bash
sudo apt update && sudo apt install -y gnupg software-properties-common curl
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list

sudo apt update
sudo apt install terraform
```

## 2. Install Terraform on Red Hat / CentOS / Rocky / AlmaLinux

### Method 1: Install using HashiCorp YUM Repository (Recommended)

```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
sudo yum install terraform
```

##  3. Install Terraform on macOS

### Method 1: Install using Homebrew (Recommended)

```bash
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```
### Method 2: Manual Installation (Binary)

```bash
curl -O https://releases.hashicorp.com/terraform/1.6.6/terraform_1.6.6_darwin_amd64.zip
unzip terraform_1.6.6_darwin_amd64.zip
sudo mv terraform /usr/local/bin/
```

##  4. Install Terraform on Windows

### Method 1: Install using Chocolatey (Recommended)

```powershell
choco install terraform
```

### Method 2: Install using Scoop

```powershell
scoop install terraform
```

### Verify Terraform Installation

```bash
terraform version
```


