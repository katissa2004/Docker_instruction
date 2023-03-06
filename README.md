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

To install the latest version, run:

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

<img src="5th.png" width="" height=""/>

Verify that the Docker Engine installation is successful by running the hello-world image (This command downloads a test image and runs it in a container. When the container runs, it prints a confirmation message and exits):

sudo docker run hello-world

<img src="6th.png" width="" height=""/>
