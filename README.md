# demo_test

Initialize vm, use public subnet in vcn, create internet gateway, add security rules

Install following packages:

sudo dnf install container-tools
sudo dnf install git


Sudo podman run -d \
-p 1521:1522 \
-p 1522:1522 \
-p 8443:8443 \
-p 27017:27017 \
-e WORKLOAD_TYPE=ATP \
-e WALLET_PASSWORD=P4ssw0rd1234! \
-e ADMIN_PASSWORD=P4ssw0rd1234!  \
--cap-add SYS_ADMIN \
--device /dev/fuse \
--name adb-free \
container-registry.oracle.com/database/adb-free:latest-23ai
