# AnyConnect-VPN-Server-Dockerized-in-ubuntu-server
AnyConnect-VPN-Server Dockerized in Ubuntu server

We dockerized and added Dockerfile to run it anywhere you want on any linux distro easily. Buggy script for configuring OpenConnect (ocserv) protocol on the server easily and automatically.

Docker Installation

    Install Docker
    Build docker image

docker build -t ocserv https://github.com/iw4p/OpenConnect-Cisco-AnyConnect-VPN-Server-OneKey-ocserv.git

    Run docker container

docker run --name ocserv --privileged -p 443:443 -p 443:443/udp -d ocserv

    Add user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName

    Change user password

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName

    Delete user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -d testUserName

    Lock user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -l testUserName

    Unlock user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -u testUserName

    Show all users and their hashed password

docker exec -ti ocserv cat /etc/ocserv/ocpasswd

Features

    Easy install
    Easy uninstall
    Add User
    Change Password
    Show All Users
    Delete User
    Lock User
    Unlock User

