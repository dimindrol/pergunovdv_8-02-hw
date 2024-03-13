# Домашнее задание к занятию "`8.02 Что такое DevOps. СI/СD`" - `Пергунов Дмитрий`

### Задание 1
1. Установили jenkins
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key |
sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```
2. Установили Go
```bash
wget https://go.dev/dl/go1.17.5.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.17.5.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> /etc/profile
```
    
### Задание 2

### Задание 3


