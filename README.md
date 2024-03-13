# Домашнее задание к занятию "`8.02 Что такое DevOps. СI/СD`" - `Пергунов Дмитрий`

### Задание 1
0. Устанавливаем JRE sudo apt-get install default-jre
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
wget https://go.dev/dl/go1.22.1.linux-amd64.tar.gz
sha256sum go1.22.1.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.22.1.linux-amd64.tar.gz

#Настройка переменных окружений
sudo nano ~/.profile
#Добавление информации в файл
export PATH=$PATH:/usr/local/go/bin
export GOPATH=$HOME/goproject
export PATH=$PATH:$GOPATH/bin
#Обновили переменные окружения
source ~/.profile
```
3. Сделали Fork репозитория https://github.com/dimindrol/8.02-DevOps.-I-D
4. 
    
### Задание 2

### Задание 3


