BootStrap: docker
From: centos:7

%post
yum -y update 
yum -y upgrade

cat << EOF >  /etc/yum.repos.d/Brave.repo
[brave-browser-beta]
name=Brave Browser Beta Channel repository
baseurl=https://brave-browser-rpm-beta.s3.brave.com/x86_64/
enabled=1
EOF

rpm --import https://brave-browser-rpm-beta.s3.brave.com/brave-core-nightly.asc
yum -y install brave-browser-beta

%runscript
brave-browser --no-sandbox "$@"
