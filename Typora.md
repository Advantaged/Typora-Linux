
# [Typora](https://support.typora.io/Typora-on-Linux/)

- [14 Best Markdown Editors for Linux](https://itsfoss.com/best-markdown-editors-linux/)


### Kubuntu:
   - In Kubuntu exist already the package "typora_0.9.86-1_amd64.deb"!


   1. To find the package use "apt search" in Terminal:
```
apt search typora
```
   2. To install use "apt install"
```
sudo apt install typora
```
   3. In case you want to change something (e.g. the "favicon" is missing) you find installed package by using "cd" and "ls":


```
cd /usr/share/typora/

ls /usr/share/typora
```

   4. Download "favicon" and inject in "installation"-folder:
```
sudo wget https://typora.io/img/favicon-64.png -O /usr/share/typora/Typora.png
```

   5. Edit with "kate" or "nano" the "desktop"-file:
```
sudo nano /usr/share/applications/typora.desktop
```

   6. Change where to look for right icon:
```
[Desktop Entry]
Name=Typora
Comment=a minimal Markdown reading & writing app. Change Log: (https://typora.io/windows/dev_release.html)
GenericName=Markdown Editor
Exec=typora %U
Icon=/usr/share/typora/Typora.png
Type=Application
StartupNotify=true
Categories=Office;WordProcessor;
MimeType=text/markdown;text/x-markdown;
```

- Save & Close **"*.desktop"**-file. Now by clicking on "KickOff" & typing "typora" appear immediately the "typora-favicon" and you can start using.
  
- [x] **Done!**
  
   **Enjoy!**


### Other Distributions:
   - In Other distributions, normally, install additional programs under "/opt/program-name" e.g.:
```
/opt/typora/
```

   - Prepare/update system and install  missing/defective "packages":
```
sudo apt update; sudo apt upgrade
sudo apt-get install -f
```

   1. If you don't know if the package is provided, search it:
```
apt search typora
```

   2. If not present, download and extract it:
```
wget https://typora.io/linux/Typora-linux-x64.tar.gz -O ~/typora.tar.gz
mkdir ~/typora
tar -xzf ~/typora.tar.gz -C ~/typora
```

   3. Download "favicon"-64 and inject to fresh "typora"-folder:
```
wget https://typora.io/img/favicon-64.png -O ~/typora/Typora.png
```

   4. Create "desktop"-file:
```
kate ~/typora/typora.desktop
```

   5. Fill the "desktop"-file for KDE5:
```
[Desktop Entry]
Name=Typora
Comment=a minimal Markdown reading & writing app. Change Log: (https://typora.io/windows/dev_release.html)
GenericName=Markdown Editor
Exec=/opt/typora/Typora
Icon=/opt/typora/Typora.png
Type=Application
StartupNotify=true
Categories=Office;WordProcessor;
MimeType=text/markdown;text/x-markdown;
```

   5.1. Fill the "desktop"-file for Gnome:
```
[Desktop Entry]
Type=Application
Name=Typora
Exec=/opt/typora/Typora
Icon=/opt/typora/Typora.png
Categories=Utility
```

   - Note: If you have another "DE" (Desktop Environment), follow appropriate instructions.
   - **Attention:** Appear to be recommended to install "gconf2" if using "Gnome"-DE!
```
sudo apt install gconf2
```

   6. Move and copy "/folder/files" to "root" (/):
```
sudo mv ~/typora /opt
sudo cp /opt/typora/typora.desktop /usr/share/applications/typora.desktop
```

   7. Assure all "Dependencies" are installed with:
```
sudo apt-get install -f
```

   8. Assure everything is at place you wish:
```
cd /opt/typora/

ls /opt/typora
```

- [x] **Done!**
  
   **Enjoy!**
   
- Here direct "Download-Links" for [Typora-linux-x64.tar.gz](https://typora.io/linux/Typora-linux-x64.tar.gz) and [Typora-linux-ia32.tar.gz](https://typora.io/linux/Typora-linux-ia32.tar.gz).
  
   
  
- **Merits to:** [skewty](https://github.com/skewty) and his "articles" on [GitHub: Linux help not correct for Ubuntu 18.04](https://github.com/typora/typora-issues/issues/1790)
  

- **P.S.:**  The **Other Distribution**-instruction are also valid for **Kubuntu**. Just use "**/usr/share/typora/**" folder **!** 