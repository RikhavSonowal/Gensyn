# Gensyn All Error Fixed
# 🚀 Gensyn Node Full Setup Guide

Ye guide aapko Gensyn node chalane ke liye complete steps degi — old cleanup se lekar Cloudflare tunnel tak. Just follow step-by-step.

---

## 📍 Old Users — First Use Cleanup

Purana setup hataane ke liye pehle ye 2 commands run karein:

```bash
sudo pkill screen
sudo rm -rf rl-swarm
```

---

## 📦 Node Setup Commands

### 1. Base Setup Script Run karo:

```bash
curl -sL https://gist.githubusercontent.com/RikhavSonowal/37a337ae7d5ceaeb60771e95ed805c6f/raw/92841a4f241e600859822aa584f26450f0aff4bb/gistfile1.txt | bash
```

### 2. Screen Session Start karo:

```bash
screen -S gensyn
```

### 3. Node Config File Download karo:

```bash
mkdir -p rl-swarm/hivemind_exp/configs/mac/
curl -sL https://raw.githubusercontent.com/RikhavSonowal/gensyn-smooth-/main/grpo-qwen-2.5-0.5b-deepseek-r1.yaml -o rl-swarm/hivemind_exp/configs/mac/grpo-qwen-2.5-0.5b-deepseek-r1.yaml
```

### 4. layout.tsx File Add karo:

```bash
mkdir -p rl-swarm/modal-login/app/
curl -sL https://raw.githubusercontent.com/RikhavSonowal/rl-swarm/main/layout.tsx -o rl-swarm/modal-login/app/layout.tsx
```

### 5. page.tsx File Add karo:

```bash
mkdir -p rl-swarm/modal-login/app/
curl -sL https://raw.githubusercontent.com/RikhavSonowal/gensyn-smooth-/main/page.tsx -o rl-swarm/modal-login/app/page.tsx
```

### 6. Project Directory me jao:

```bash
cd rl-swarm
```

### 7. Python Virtual Environment Setup karo:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 8. Node Ko Start Karo:

```bash
./run_rl_swarm.sh
```

---

## 🌐 Install Cloudflare Tunnel (Optional)

Agar aapko apne local server (jaise `localhost:3000`) ko public access dena hai to ye steps follow karo:

### 1. Cloudflare Tunnel Script Install Karo:

```bash
curl -sL https://raw.githubusercontent.com/RikhavSonowal/cloudflare/main/install-firewall-cloudflared.sh | bash
```

### 2. `.deb` Package Install Karo:

```bash
sudo dpkg -i cloudflared-linux-amd64.deb
```

### 3. Tunnel Start Karo:

```bash
cloudflared tunnel --url http://localhost:3000
```

---

## ✅ Tips

- `screen` ko detach karne ke liye:  
  Press `Ctrl + A` then `D`
  
- Wapas join hone ke liye:  
  ```bash
  screen -r gensyn
  ```

- Node ko band karne ke liye:  
  ```bash
  sudo pkill screen
  ```

- Folder clean karne ke liye:  
  ```bash
  sudo rm -rf rl-swarm
  ```

---

## 🙋 Maintained By

[Rikhav Sonowal](https://github.com/RikhavSonowal)

---

## ❤️ Join Our Community

👉 **Telegram Channel**: [https://t.me/CryptoRikhav](https://t.me/CryptoRikhav)
