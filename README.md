this repo help you setup new linux machine with claude, espicially you are a robotics engineer/researcher setting up a new personal ubunut machine.

### install claude
```
curl -fsSL https://claude.ai/install.sh | bash
```

### set claude
```
cat >> ~/.bashrc << 'EOF'
export ANTHROPIC_BASE_URL="https://your-org/api"
export ANTHROPIC_AUTH_TOKEN="your-api-token-here"
alias cds="claude --dangerously-skip-permissions"
EOF
source ~/.bashrc
```

### install prompt
```
passcode is xxx, help me to install 
- cursor, google chrome, cloudflared, qq, wechat, zsh, oh my zsh(install auto-suggestion plugin and copypath plugin), vim. add a zsh command at the end of ~/.bashrc . 

- generate ~/.ssh/id_ed25519
finally help me to login github. install terminator. set terminate as default terminal. 
install things which is necessary for `gh auth login`. 

- download screenshot app snipaste. and add it autostart service when boot the machine.

- set vim as the default editor for git commit -s

- do not upgrade the linux kernel
```

### github login
```
gh auth login
```

### install ros2 humble
```
- install ros2 humble
```

### install uv
```
- install uv (python package manager)
```

### install net-tools
```
- install net-tools
```

### install docker

**Method 1: Docker official source via Alibaba Cloud mirror (recommended)**

```bash
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg git-lfs

sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://mirrors.aliyun.com/docker-ce/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/docker.gpg] https://mirrors.aliyun.com/docker-ce/linux/ubuntu jammy stable" | sudo tee /etc/apt/sources.list.d/docker.list

sudo apt-get update
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin git-lfs
```

**Method 2: Ubuntu built-in packages (simple)**

```bash
sudo apt-get update
sudo apt-get install -y docker.io docker-compose-v2 git-lfs
```

**Post-install (both methods):**

```bash
sudo usermod -aG docker $USER
newgrp docker
git lfs install
```
