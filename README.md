# Proxmoxxxing

A homelab documentation (i just need a job 😭).

> [!NOTE]
> **Proxmoxxxing** is not yet done, I still have goals set to improve my homelab.

## Proxmox

Set up **Proxmox OS** for server virtualization. I did a basic setup and install **Fedora Server** using **QEMU** in a Vitrual Machine. Due to limited capacity of my hardware, sticking to one virtual machine will do the work.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cf87c01b-e593-4650-aaed-7b3ae5ca98c6" />

## Fedora Server

Installed **Fedora Server** on a Virtual Machine instance, this server would be my **DevOps** experimentation server. My goal is to deploy a **Springboot Server** containerized in **Docker**.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/19165cff-85f3-4961-88b8-b0d0d70ef4da" />

## Tailscale

Tailscale is a powerful tool that allows me to have privilege access across devices. I include this because of how flexible and portable Tailscale. The screenshot below shows that I SSH to my **Fedora Server** through Tailscale. 

<img width="1920" height="1080" alt="2026-09-30-085719_hyprshot" src="https://github.com/user-attachments/assets/04e16b5d-c2b3-4704-aca9-08a1fc0c40a3" />

## LXC Setup

It is my first time setting up **LXC**(Linux Containers) for **pi-hole**. But I fail first because it cannot run 'apt' commands due to the fact that it cannot get installable packages on **Debian Mirror Servers**.

<img width="1890" height="1002" alt="image" src="https://github.com/user-attachments/assets/207631e1-5107-437e-8c99-6e93c3f1c560" />

Now I found the root cause as shown in the image below. I didn't setup the **DNS Domain** and **DNS Server** because I rely on **use host settings**. But the default of **use host settings** comes from **Tailscale**.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d47add40-9710-43d4-93c8-31ac915008c5" />

I can either run `tailscale up --accept-dns=false` or set things **Manually**. I choose the **manual** way to familiarize my self more on setting up DNS Domain and DNS Server using IP addresses.
