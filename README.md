# Домашнее задание к занятию "`8.02 Что такое DevOps. СI/СD`" - `Пергунов Дмитрий`

### Задание 1
1. Установил сервер и необходимые компоненты используя [Ссылка на Решение (Vagrant file)](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/main/Vagrantfile)
2. Настроил Jenkins подулючил репозиторий [Ссылка на Решение (GIT)]([https://github.com/netology-code/sdvps-materials.git) , далее настроил сборку
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
1. Создали новый проект Pipeline
2. Переписали сборку из задания 1 на declarative в виде кода [Ссылка на КОД (PIPELINE)](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/main/pipeline)
3. Решение:
   
![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/aa9f5dcb3a412cd3c5111aa0447b721a6b491752/img/%D0%98%D1%81%D1%82%D0%BE%D1%80%D0%B8%D1%8F%20%D1%81%D0%B1%D0%BE%D1%80%D0%BE%D0%BA.png)`

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/aa9f5dcb3a412cd3c5111aa0447b721a6b491752/img/stage%20view.png)`

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/aa9f5dcb3a412cd3c5111aa0447b721a6b491752/img/%D1%88%D0%B0%D0%B3%D0%B8%20%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F.png)`

### Задание 3
1. Nexus установлен.
2. Создали RAW_hosted репозиторий http://192.168.56.10:8081/repository/Raw_hosted/
3. Изменили pipeline, чтобы собирался docker образ [Ссылка на КОД (PIPELINE GO)](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/main/GO_PIPE_CODE)
4. Загрузили Файл на сервер результат

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/28ec3193ce43bcbdcb9a577070cc1f8adb7f8d79/img/GO_PIPE_LOG.png)`

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/28ec3193ce43bcbdcb9a577070cc1f8adb7f8d79/img/GO_PIPE_STAGE.png)`

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/28ec3193ce43bcbdcb9a577070cc1f8adb7f8d79/img/GO_PIPE_%D0%B8%D1%81%D1%82%D0%BE%D1%80%D0%B8%D1%8F%20%D1%81%D0%B1%D0%BE%D1%80%D0%BE%D0%BA.png)`

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-02-hw/blob/28ec3193ce43bcbdcb9a577070cc1f8adb7f8d79/img/NEXUS_PIPE_GO.png)`




