# Prep for installation
- Backup existing system and ensure backups are readable
- prepare info for installation
    - firefox account name and password
    - email account access info and password
    
# Initial OS installation and boot setup
- fix fstab settings
    - add noatime flag to ssd volumes
    - add mountpoints for:
        - efi
        - virtuallbox
        - workspace

# Initial manual install via command line or muon
- ansible
- git
- 

```bash
sudo apt update
sudo apt install git
sudo apt install ansible
mkdir desktop-config
cd desktop-config
#
# if browser is available, the next 3 steps can be accomplished by loggin into githu and cloning repository
#
git config --global user.name "Ogden Boone"
git config --global user.email o.boone@gmail.com
git clone https://github.com/oiboone/desktop-config
#
sudo ansible-playbook main.yml
```

# Connect to samba share on raspberry pi server
name: 192.168.0.4
server: 192.168.0.4
address: smb://192.168.0.4/
folder: share

# Configuration of Firefox and Thunderbird
- Set up firefox account
- Install these firefox addins:
    - lastpass (or possibly bitwarden in the future)
    - ublock origin
    - https everywhere
- Install these thunderbird addons
    - lightning calendar
    - google provider
    - enigmail
    
# setup putty and remmina config files
- Now part of ansible setup (config.yml)

# setup commonly used latex packages
- Now part of ansible setup (config.yml)

# zotero customization

- goto <https://www.zotero.org/download/connectors> and install connectors for firefox and chrome.
- goto <https://github.com/retorquere/zotero-better-bibtex/releases/tag/v5.2.22> and download *.xpi file to downloads directory
- open zotero and 
    - install libreoffice addin
    - install better bibtex 
    - log into zotero account in edit->preferences