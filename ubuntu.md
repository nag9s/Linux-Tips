sudo passwd root

apt-get update && //apt-get install -y lubuntu-desktop
sudo apt install gnome-session gdm3
sudo apt install tasksel && sudo tasksel install ubuntu-desktop && sudo apt-get install tightvncserver
apt-get install xfonts-base && sudo apt-get install xrdp
//sudo apt-get install xfce4 xfce4-goodies
//echo xfce4-session >~/.xsession

nano /etc/gdm3/custom.conf
add under the [daemon] AllowRoot=true

nano /etc/pam.d/gdm-password

comment out the following line, so that it looks like
#auth required pam_succeed_if.so user != root quiet_success
sudo apt-get install chrome-gnome-shell
sudo service xrdp restart

reboot

Then install handy gnome extensions
https://extensions.gnome.org

#### popular extensions
Dash to Dock https://extensions.gnome.org/extension/307/dash-to-dock/
Applications-menu https://extensions.gnome.org/extension/6/applications-menu/
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MDI2MzM0OThdfQ==
-->