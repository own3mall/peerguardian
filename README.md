# peerguardian
Peerguardian Linux Fixes

## Add to `/etc/sysctl.conf`:
```
sudo -i
cat << EOF | sudo tee -a /etc/sysctl.conf
net.core.rmem_default=8388608
net.core.wmem_default=8388608
net.core.rmem_max=16777216
net.core.wmem_max=16777216
EOF

# Reload settings to apply them now
sudo sysctl -p
```
