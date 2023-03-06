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

Use the following command to set up the repository:

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
<img src="3rd.png" width="" height=""/>

Update the apt package index:

sudo apt-get update

<img src="4th.png" width="" height=""/>
