# Installation instructions

```bash
cd /tmp/
git clone https://github.com/thesqual92/earnapp_pizero.git
cd earnapp_pizero/
```

# Binary installation
```bash
gunzip -d earnapp_for_pizero.gz
sudo cp earnapp_for_pizero /usr/bin/earnapp
sudo chmod +x /usr/bin/earnapp
```
# Get Earnapp configuration from another device 
#Copy a /etc/earnapp from another device already linked to earnapp (move the /etc/earnapp since it has a unique UUID that can only work on one device simultaneously)

#Copy and install the earnapp service

# Installation of the earnapp service
```bash
sudo cp earnapp.service /etc/systemd/system/
sudo systemctl enable earnapp
sudo systemctl start earnapp
sudo systemctl status earnapp 
```
expected output for ```bash sudo systemctl status earnapp ```
earnapp.service - EarnApp
     Loaded: loaded (/etc/systemd/system/earnapp.service; enabled; preset: enabled)
     Active: active (running) since Thu 2026-08-13 13:41:54 CEST; 9min ago
 Invocation: e777924287d84031a5a517ed6c50bbad
   Main PID: 4789 (earnapp)
      Tasks: 11 (limit: 449)
        CPU: 19.253s
     CGroup: /system.slice/earnapp.service
             └─4789 /usr/bin/earnapp run
             
```bash
/usr/bin/earnapp status
```
Expected output : "✔ Current status: enabled"
