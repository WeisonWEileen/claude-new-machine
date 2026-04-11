this repo help you setup new linux machine with cladue

### install claude
```
curl -fsSL https://claude.ai/install.sh | bash
```

### set claude
```
cat >> ~/.bashrc << 'EOF'
export ANTHROPIC_BASE_URL="https://your-company/api"
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
```

### github login
```
gh auth login
```
