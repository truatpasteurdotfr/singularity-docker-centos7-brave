BootStrap: docker
From: centos:7

%post
yum -y update 
yum -y upgrade

# https://brave-browser.readthedocs.io/en/latest/installing-brave.html#linux

cat << EOF > /etc/yum.repos.d/brave-browser-release.repo
[brave-browser-release]
name=Brave Browser Release Channel repository
baseurl=https://brave-browser-rpm-release.s3.brave.com/x86_64/
enabled=1
EOF

yum -y install brave-keyring brave-browser

%runscript
# --no-sandbox is a security risk
brave-browser --no-sandbox "$@"

