

![image](https://github.com/user-attachments/assets/c1734478-7ba8-42ae-882a-4b5a90f43556)



 * [Topluluk kanalımız](https://t.me/corenodechat)<br>
 * [Topluluk Twitter](https://twitter.com/corenodeHQ)<br>
 * [Discord](https://discord.gg/NkmNypKZQG)<br>

### Sistem paketlerini güncelleyelim ve gerekli bağımlılıkları yükleyelim
```
sudo apt update && sudo apt install -y apt-transport-https ca-certificates curl gnupg lsb-release && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io && sudo systemctl start docker && sudo systemctl enable docker

```

### WALLETADRESS kısmına EVM cüzdan adresimizi yazıp kodu çalıştıralım
```
sudo docker pull neovaprotocol/provider && sudo docker run -d --name neova --restart always -e EVM_ADDRESS=evmadres neovaprotocol/provider

```

### Logları kontrol edelim
```
docker logs -f neova
```
