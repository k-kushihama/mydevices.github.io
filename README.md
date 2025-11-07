# 🖥️ My Gear & Infrastructure

このリポジトリは，使用しているワークステーション，サーバー，および関連するインフラストラクチャの構成を管理・文書化するために作成．

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

### 💻 Main Desktop


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

### Laptop

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

### 🏠 Home Lab

自宅サーバー（Proxmox VE）で稼働しているVMやコンテナです．

| カテゴリ | スペック | 備考 |
| :--- | :--- | :--- |
| **Model** | MacBook Pro 14インチ | M3 Max |
| **OS** | macOS Sonoma | |
| **CPU/GPU** | Apple M3 Max | 16コアCPU / 40コアGPU |
| **RAM** | 64GB | ユニファイドメモリ |
| **Storage** | 2TB SSD | |



### 🌐 Cloud (VPS)

外部公開用のVPS（Virtual Private Server）です．

| プロバイダ | プラン | OS | 主な役割 |
| :--- | :--- | :--- | :--- |
| **Contabo** | Cloud VPS M | Ubuntu 22.04 LTS | Webサーバー (Nginx), リバースプロキシ |
| **AWS** | EC2 (t3.micro) | Amazon Linux 2 | S3バックアップ用踏み台 |
| **Vultr** | High Frequency | Debian 12 | VPN (WireGuard) |
