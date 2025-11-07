# 🖥️ My Gear & Infrastructure

このリポジトリは，私が使用しているワークステーション，サーバー，および関連するインフラストラクチャの構成を管理・文書化するためのものです．

<p align="center">
  <img src="https://img.shields.io/badge/OS-Windows_11-blue?logo=windows11" alt="Windows 11">
  <img src="https://img.shields.io/badge/OS-macOS_Sonoma-grey?logo=apple" alt="macOS Sonoma">
  <img src="https://img.shields.io/badge/OS-Ubuntu-orange?logo=ubuntu" alt="Ubuntu">
  <img src="https://img.shields.io/badge/OS-Proxmox-blueviolet?logo=proxmox" alt="Proxmox">
  <img src="https://img.shields.io/badge/CPU-Intel-blue?logo=intel" alt="Intel CPU">
  <img src="https://img.shields.io/badge/GPU-NVIDIA-green?logo=nvidia" alt="NVIDIA GPU">
  <img src="https://img.shields.io/badge/Virtualization-Docker-blue?logo=docker" alt="Docker">
</p>

---

##  workstations ｜ ワークステーション

メインの作業環境です．

### 💻 Main Desktop (Kaguya)

開発とデザインのコアとなるマシンです．

| カテゴリ | スペック | 備考 |
| :--- | :--- | :--- |
| **OS** | Windows 11 Pro | `23H2` |
| **CPU** | Intel Core i9-13900K | 24コア / 32スレッド |
| **GPU** | NVIDIA GeForce RTX 4090 | 24GB GDDR6X |
| **RAM** | 64GB DDR5 (32GB x2) | CORSAIR VENGEANCE @ 5600MHz |
| **Storage (OS)** | 2TB NVMe SSD | Samsung 990 PRO |
| **Storage (Data)** | 4TB NVMe SSD | Crucial P5 Plus |
| **Monitor 1** | 32" 4K 144Hz | Dell G3223Q |
| **Monitor 2** | 27" WQHD 165Hz | (サブモニター) |

### portátil ｜ ラップトップ (Miyuki)

外出先やミーティングで使用するポータブル環境です．

| カテゴリ | スペック | 備考 |
| :--- | :--- | :--- |
| **Model** | MacBook Pro 14インチ | M3 Max |
| **OS** | macOS Sonoma | |
| **CPU/GPU** | Apple M3 Max | 16コアCPU / 40コアGPU |
| **RAM** | 64GB | ユニファイドメモリ |
| **Storage** | 2TB SSD | |

---

## ☁️ Server Infrastructure ｜ サーバー環境

自宅およびクラウドで稼働しているサーバー群です．

### 🏠 Home Lab (Fujiwara)

自宅サーバー（Proxmox VE）で稼働しているVMやコンテナです．

> **ホストマシン スペック (Proxmox VE Host):**
> * **CPU:** AMD Ryzen 7 5700X
> * **RAM:** 128GB DDR4 ECC
> * **OS:** Proxmox VE 8.1
> * **Storage (PVE):** 1TB NVMe SSD (ZFS Mirror)
> * **Storage (VMs):** 4TB SATA SSD (RAID 1)

| VM/Container (ID) | サービス名 | OS / Base | CPU/RAM | IP (Internal) | 概要 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `VM 100` | **Gateway** | OPNsense | 2C / 4GB | `192.168.1.1` | ファイアウォール, VPN |
| `VM 101` | **PBX-Server** | Debian 12 | 4C / 8GB | `192.168.1.10` | Asterisk (例: Clocall連携) |
| `VM 102` | **Dev-Server** | Ubuntu 22.04 | 8C / 16GB | `192.168.1.15` | 開発用VM (Docker) |
| `LXC 200` | **AdGuard** | Ubuntu 22.04 | 1C / 512MB | `192.168.1.5` | DNS広告ブロック |
| `LXC 201` | **CI/CD** | Ubuntu 22.04 | 2C / 2GB | `192.168.1.20` | GitLab Runner |

### 🌐 Cloud (VPS)

外部公開用のVPS（Virtual Private Server）です．

| プロバイダ | プラン | OS | 主な役割 |
| :--- | :--- | :--- | :--- |
| **Contabo** | Cloud VPS M | Ubuntu 22.04 LTS | Webサーバー (Nginx), リバースプロキシ |
| **AWS** | EC2 (t3.micro) | Amazon Linux 2 | S3バックアップ用踏み台 |
| **Vultr** | High Frequency | Debian 12 | VPN (WireGuard) |
