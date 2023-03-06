1. Install Docker Engine on Ubuntu

Update the apt package index and install packages to allow apt to use a repository over HTTPS:

 sudo apt-get update
 sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \

<img src="1st.png" width="" height=""/>

Add Docker’s official GPG key:

sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

<img src="2nd.png" width="" height=""/>
