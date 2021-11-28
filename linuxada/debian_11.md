-- layout: default
-- title: Debian 11 Bullseye
-- summary: Information about Debian 11 Bullseye repository
### Enabled CPU architectures
x86_64 and arm64

### List of available packages
[List of available packages and their statuses](https://build.opensuse.org/project/monitor/home:thindil?defaults=0&succeeded=1&failed=1&unresolvable=1&broken=1&blocked=1&dispatching=1&scheduled=1&building=1&finished=1&signing=1&locked=1&deleting=1&arch_aarch64=1&arch_armv7l=1&arch_x86_64=1a&repo_Debian_11=1)

### Enabling the repository

*Note: Keep in mind that the owner of the key may distribute updates, packages and
repositories that your system will trust ([more information](https://wiki.debian.org/SecureApt)).* 

In a console enter:

    echo 'deb http://download.opensuse.org/repositories/home:/thindil/Debian_11/ /' | sudo tee /etc/apt/sources.list.d/home:thindil.list

    curl -fsSL https://download.opensuse.org/repositories/home:thindil/Debian_11/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_thindil.gpg > /dev/null

    sudo apt update

You can also skip this step and download the selected package(s) directory, but then you will not have option to obtain automatically updates to them.
