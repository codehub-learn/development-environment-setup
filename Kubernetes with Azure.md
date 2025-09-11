# Kubernetes on Windows

1. Download and install **as an Administrator** the Latest MSI of the Azure CLI from here -> **[Azure CLI 64-bit](https://aka.ms/installazurecliwindowsx64)** or **[Azure CLI 32-bit](https://aka.ms/installazurecliwindows)**

2. Simply download the latest version of kubectl (without installing it) from here -> **[kubectl](https://dl.k8s.io/release/v1.30.0/bin/windows/amd64/kubectl.exe)**.\
*(Further instructions will be given inside the classroom)*

# 

# Kubernetes on Linux

1. Download and install Azure CLI using one of the methods described in the official guide -> **[How to Install Azure CLI on Linux](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt)**

2. Simply download the latest kubectl version (without installing it) using the following command:
```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```
