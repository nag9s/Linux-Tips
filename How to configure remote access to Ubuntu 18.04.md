
## Introduction

This guide clarifies exactly how we can configure remote desktop computer accessibility on Ubuntu 18.04 as well as consequently allowing gaining access to Ubuntu utilizing RDP programs either from home windows or from mac. 

There are a number of reasons that you may intend to remote connect to your Ubuntu computer system. Probably you're at job as well as need to log right into your home computer. Additionally, you could have an Ubuntu COMPUTER in one area, your Windows PC in another. Perhaps you want to run updates on Ubuntu, or gain access to documents. This likewise makes good sense in case if we wish to perform some actives making use of GUI. 

## Prerequisites

We need the following toolset before we proceed further

* Ubuntu 18.04 compute instance
* Mobaxterm tool

## Changing the password

Break your documentation into logical sections. Use heading 2 for major section headers. Preface steps with step numbers. Use numerals, not words. Use Title Case.

Code blocks are prefaced by four spaces. Command lines should be prefaced by a prompt. If a linux root user, use a hash prompt. If a standard user, use a dollar sign. If PowerShell or Windows cmd.exe use the appropriate prompt to preface your commands.

Standard distribution comes with root prompt. Please change password if needed

    # sudo passwd root



## Installing Desktop Environment

A typical document may have as few as two, and rarely more than ten major sections.

Inline code should be wrapped by backticks. For example, you could instruct the user to perform `ls` in your narrative. This can be convenient, but code blocks are preferred. Reserve backticks for actual commands. Do not use backticks are a replacement for bold or italics. Use bold for the names of GUI objects, such as buttons, icons, or input fields. Use italics for the information to be typed. For example, this would be correct:

* Click the **Done** button, then type :key_win:+:key_r:.
* Type _cmd.exe_ in the **Open** field, then click **OK**.
* When the command window opens, type `dir` at the prompt.

### Subsections for minor sub-steps

Each major Heading 2 section may also contain multiple subsections. Use Heading 3 for subsections. Use sentence case for subsections.

### Another subsection

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sit amet blandit arcu. Phasellus ac massa vel nisi sodales pretium id non nibh. Proin et quam mattis, dapibus turpis nec, vestibulum justo. Morbi vitae viverra metus. Integer blandit accumsan ipsum, vitae tincidunt sem lobortis ac. Sed dictum in elit vel cursus. Nunc commodo massa mi, vel imperdiet nunc volutpat vestibulum. Morbi rhoncus magna non aliquet faucibus. Curabitur ac vulputate urna, quis condimentum velit. Vivamus fringilla porttitor pretium. Mauris convallis turpis nisi, eget pharetra est lacinia at. Maecenas sed pharetra sapien. Praesent et eros pharetra ipsum iaculis aliquam.

## Installing the VNC Server

This is the last major section of this template. Your document may have more sections.

## Installing the Fonts
## Installing the RDP Framework such XRDP
## Updating Configuration
## Restarting XRDP
## Access the instance over RDP

## Conclusion

Refresh the reader on what they have accomplished and what capabilities they have enabled. If appropriate, you may consider some of the following subsections.

### Further steps

This is a good place to link additional tutorials or recommend some standard settings.

### References

Consider including a few bullet points with links more documentation or comprehensive references. For example:

* Links to GitHub projects
* Links to Linux distribution documentation
* Links to the application documentation

sudo passwd root

apt-get update && apt-get install -y lubuntu-desktop
sudo apt install gnome-session gdm3
sudo apt install tasksel
sudo tasksel install ubuntu-desktop

sudo apt-get install tightvncserver
apt-get install xfonts-base
sudo apt-get install xrdp
//sudo apt-get install xfce4 xfce4-goodies
//echo xfce4-session >~/.xsession

nano /etc/gdm3/custom.conf
add under the [daemon] AllowRoot=true

nano /etc/pam.d/gdm-password

comment out the following line, so that it looks like
# auth required pam_succeed_if.so user != root quiet_success

sudo service xrdp restart





access the instance from windows rdp with the ip address
