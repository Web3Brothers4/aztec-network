# aztec-network
A step by step guide on How to Run `Sequencer Node` on Aztec Network Testnet & Earn `Apprentice` Role.

## Hardware Requirements
* **Sequencer Node**: 8 cores CPU, 16GB RAM, 100GB+ SSD
* **Prover Node**: Requiring ~40x machines with 16 cores and 128GB RAM


## 1. Install Dependecies
* Update packages:
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

* Install Packages:
```bash
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```

* Install Docker:
```bash
sudo apt update -y && sudo apt upgrade -y
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y && sudo apt upgrade -y

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Test Docker
sudo docker run hello-world

sudo systemctl enable docker
sudo systemctl restart docker

```
if you using google cloud than use 4th command before 5th command if you using normal vps than 5th command directly 
2. sudo usermod -aG docker $USER
```

NOW OPEN A NEW TERMINAL OR DUPLICATE
```
## 3. Install Aztec Tools
```bash
bash -i <(curl -s https://install.aztec.network)
```
4. sudo usermod -aG docker $USER
```
## 5. Update Aztec
```bash
aztec-up alpha-testnet
```
