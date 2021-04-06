## Docker Pi-Hole for RaspberryPi

<p align="center">
        <img src="icon.png" alt="PNG" height="300px" />
</p>

### Requeriments
- Raspberry Pi / NanoPi NEO2 or NEO3
- Raspbian OS / DietPi
- Service docker running

### Install Docker
    sudo apt update
    sudo apt upgrade -y
    sudo apt install -y libffi-dev libssl-dev python3 python3-pip
    sudo curl -sSL https://get.docker.com | sh
    sudo usermod -aG docker pi
    sudo apt install -y docker-compose

### Add lines in /boot/config.txt (RaspberryPi 3)
    arm_freq=1200
    arm_freq_min=700
    core_freq=400
    core_freq_min=250
    sdram_freq=450
    sdram_freq_min=400

### Edit vars in docker-compose.yml
Edit the following variables, with the correct interface and IP of the RasPi.

    INTERFACE:
    ServerIP:


### Running
    docker-compose up -d

### Check
    docker ps -a

### One-Step Automated Install mode native
Those who want to get started quickly and conveniently may install Pi-hole using the following command:

    curl -sSL https://install.pi-hole.net | bash

### Lists to add to Adlist group management
    https://dbl.oisd.nl
    https://sysctl.org/cameleon/hosts
    https://s3.amazonaws.com/lists.disconnect.me/simple_tracking.txt
    https://s3.amazonaws.com/lists.disconnect.me/simple_ad.txt
    http://winhelp2002.mvps.org/hosts.txt
    https://s3.amazonaws.com/lists.disconnect.me/simple_malvertising.txt
    https://someonewhocares.org/hosts/hosts
    https://adaway.org/hosts.txt
    https://pgl.yoyo.org/adservers/serverlist.php?hostformat=hosts&showintro=0&mimetype=plaintext
    https://v.firebog.net/hosts/Easyprivacy.txt
    https://v.firebog.net/hosts/AdguardDNS.txt
    https://v.firebog.net/hosts/Easylist.txt
    https://raw.githubusercontent.com/Perflyst/PiHoleBlocklist/master/AmazonFireTV.txt
    https://raw.githubusercontent.com/Perflyst/PiHoleBlocklist/master/SmartTV.txt
    https://www.malwaredomainlist.com/hostslist/hosts.txt
    https://phishing.army/download/phishing_army_blocklist_extended.txt
    https://raw.githubusercontent.com/Spam404/lists/master/main-blacklist.txt
    https://hostfiles.frogeye.fr/firstparty-trackers-hosts.txt
    https://zerodot1.gitlab.io/CoinBlockerLists/hosts_browser
    https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.Spam/hosts
    https://raw.githubusercontent.com/FadeMind/hosts.extras/master/UncheckyAds/hosts
    https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.Risk/hosts
    https://raw.githubusercontent.com/anudeepND/blacklist/master/adservers.txt
    https://www.github.developerdan.com/hosts/lists/ads-and-tracking-extended.txt
    https://raw.githubusercontent.com/crazy-max/WindowsSpyBlocker/master/data/hosts/spy.txt
    https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts
    https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/urlhaus-filter-domains.txt
    https://raw.githubusercontent.com/kboghdady/youTube_ads_4_pi-hole/master/youtubelist.txt
    https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/outapzazaList.txt
    https://raw.githubusercontent.com/outapzaza/blocklist/master/fingerprintblock.txt
    https://raw.githubusercontent.com/outapzaza/blocklist/master/serverblocklist.txt
    https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/outapzazaRegex.txt
    https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/NSABlocklist.txt
    https://raw.githubusercontent.com/hoshsadiq/adblock-nocoin-list/master/hosts.txt
    https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/AndroidTracking.txt
