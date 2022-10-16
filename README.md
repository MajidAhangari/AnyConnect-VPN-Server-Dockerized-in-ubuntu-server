# AnyConnect-VPN-Server-Dockerized-in-ubuntu-server
AnyConnect-VPN-Server Dockerized in Ubuntu server

We dockerized and added Dockerfile to run it anywhere you want on any linux distro easily. Buggy script for configuring OpenConnect (ocserv) protocol on the server easily and automatically.

Docker Installation

    1.Install Docker
    2.Build docker image

docker build -t ocserv https://github.com/iw4p/OpenConnect-Cisco-AnyConnect-VPN-Server-OneKey-ocserv.git

    3.Run docker container

docker run --name ocserv --privileged -p 443:443 -p 443:443/udp -d ocserv

    4.Add user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName

    5.Change user password

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName

    6.Delete user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -d testUserName

    7.Lock user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -l testUserName

    8.Unlock user

docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -u testUserName

    9.Show all users and their hashed password

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

in the nano /etc/ocserv/ocserv.conf  Set the number of devices a user is able to log in from at the same time. Default is 2. Set to zero for unlimited.

max-same-clients = 2


