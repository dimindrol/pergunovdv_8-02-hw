# Домашнее задание к занятию "`8.02 Что такое DevOps. СI/СD`" - `Пергунов Дмитрий`

### Задание 1
1. Установил сервер и необходимые компоненты используя [Ссылка на Решение (Vagrant file)](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/main/Vagrantfile)
2. Настроил Jenkins подулючил репозиторий [Ссылка на Решение (GIT)]([https://github.com/netology-code/sdvps-materials.git), далее настроил сборку
```bash
/usr/local/go/bin/go test .
docker build . -t ubuntu-bionic:8082/hello-world:v$BUILD_NUMBER
docker login ubuntu-bionic:8082 -u admin -p admin && docker push ubuntu-bionic:8082/hello-world:v$BUILD_NUMBER && docker logout
```
3. Создал репозиторий Jenkins и разрешил доступ по порту 8082 http://192.168.56.10:8081/#admin/repository/repositories:docker-image
4. Запустил Сборку
5. Решение:

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/e3e9b08d11d010c8e63556e2499d9f442a6a2264/img/jencins.png)`

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/83fc29618165bcdb2fe97be915f871767eb0f2c1/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0.png)`

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/e3e9b08d11d010c8e63556e2499d9f442a6a2264/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024.png)`

 
### Задание 2

### Задание 3


