# ubuntu-install
My Script to install ubuntu

### Installing Git
```
sudo apt-get install git   
```

### Installing Chrome
```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
```


### Installing Vscode
```
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
```
### Installing ZSH with oh-my-zsh
```
sudo apt install zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### Cloudflare warp-cli
First, install the repository's GPG key:
```
curl https://pkg.cloudflareclient.com/pubkey.gpg | sudo gpg --yes --dearmor --output /usr/share/keyrings/cloudflare-warp-archive-keyring.gpg
```
Then add the repository to your machine's apt sources:
```
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/cloudflare-client.list
```
```
sudo apt update
sudo apt install cloudflare-warp
warp-cli register
warp-cli connect
```

### Neovim
```
sudo apt install neovim
```
### NPM and NodeJs using NVM
Currently using : v16.15.1 (npm v8.11.0)
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
nvm install --lts
```

### Postman
```
snap install postman
```

### MongoDB Compass
```
wget https://downloads.mongodb.com/compass/mongodb-compass_1.32.2_amd64.deb
sudo dpkg -i mongodb-compass_1.32.2_amd64.deb
```
 if libconfig-2-4 is absent use this command first
```
sudo apt-get install libgconf-2-4
apt --fix-broken install

```

### Brave Browser
```
sudo apt install apt-transport-https curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser
```

