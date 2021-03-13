#! /bin/bash
sudo apt install libpci-dev
printf "downloading salad.io,chrome,vnc, root pass: 1234" >&2
sudo useradd -m ALOK
sudo adduser ALOK sudo
echo 'ALOK:1234' | sudo chpasswd
sed -i 's/\/bin\/sh/\/bin\/bash/g' /etc/passwd
wget https://dl.google.com/linux/direct/chrome-remote-desktop_current_amd64.deb
sudo dpkg --install chrome-remote-desktop_current_amd64.deb
sudo apt install --assume-yes --fix-broken
sudo DEBIAN_FRONTEND=noninteractive \
apt install --assume-yes xfce4 desktop-base
sudo bash -c 'echo "exec /etc/X11/Xsession /usr/bin/xfce4-session" > /etc/chrome-remote-desktop-session'  
sudo systemctl disable lightdm.service
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
wget https://github.com/SaladTechnologies/salad-applications/releases/download/0.5.1/Salad-0.5.1_amd64.deb
sudo dpkg --install Salad-0.5.1_amd64.deb
sudo dpkg --install google-chrome-stable_current_amd64.deb
sudo apt install nautilus nano -y 
sudo apt --fix-broken install
sudo adduser ALOK chrome-remote-desktop
printf '\nCheck https://remotedesktop.google.com/headless  copy debian/linux command and send here\n'
read -p "Paste Here: " CRP
su - ALOK -c """$CRP"""
printf 'https://remotedesktop.google.com/access/'
