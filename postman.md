# How to install Postman

Step 1. Download the app (linux(x64)) from this website:

```bash
https://www.postman.com/downloads/?authFlowId=01731e31-aebe-484d-a111-7f55812a16c9
```
🧱 Step 2: Extract Postman into /opt

```bash
sudo tar -xzf ~/Downloads/postman-linux-x64.tar.gz -C /opt
```
This will unpack all the real Postman files into /opt/Postman.

🧩 Step 3: Confirm it extracted correctly

```bash
ls /opt/Postman
```

✅ You should see files and folders like:

```bash
Postman app
```

⚙️ Step 4: Create a shortcut command

```bash
sudo ln -sf /opt/Postman/Postman /usr/bin/postman
```
The -sf makes sure it replaces any old or broken link.

🚀 Step 5: Launch Postman

```
postman
```

🧩 Step 5 (Optional): Add to Application Menu

```bash
cat <<EOF | sudo tee /usr/share/applications/postman.desktop
[Desktop Entry]
Name=Postman
Exec=postman
Icon=/opt/Postman/app/resources/app/assets/icon.png
Type=Application
Categories=Development;
EOF
```
Now search “Postman” in your app menu — it should appear 🎯