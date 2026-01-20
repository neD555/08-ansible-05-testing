### Домашнее задание к занятию 5 «Тестирование roles».

### Подготовка к выполнению.

Установите molecule и его драйвера: pip3 install "molecule molecule_docker molecule_podman.

Выполните docker pull aragast/netology:latest — это образ с podman, tox и несколькими пайтонами (3.7 и 3.9) внутри.

### Основная часть.

Ваша цель — настроить тестирование ваших ролей.

Задача — сделать сценарии тестирования для vector.

Ожидаемый результат — все сценарии успешно проходят тестирование ролей.

### Molecule.

1.Запустите molecule test -s ubuntu_xenial (или с любым другим сценарием, не имеет значения) внутри корневой директории clickhouse-role, посмотрите на вывод команды. Данная команда может отработать с ошибками или не отработать вовсе, это нормально. Наша цель - посмотреть как другие в реальном мире используют молекулу И из чего может состоять сценарий тестирования.

2.Перейдите в каталог с ролью vector-role и создайте сценарий тестирования по умолчанию при помощи molecule init scenario --driver-name docker.

3.Добавьте несколько разных дистрибутивов (oraclelinux:8, ubuntu:latest) для инстансов и протестируйте роль, исправьте найденные ошибки, если они есть.

4.Добавьте несколько assert в verify.yml-файл для проверки работоспособности vector-role (проверка, что конфиг валидный, проверка успешности запуска и др.).

5.Запустите тестирование роли повторно и проверьте, что оно прошло успешно.

6.Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

### Tox.

1.Добавьте в директорию с vector-role файлы из директории.

2.Запустите docker run --privileged=True -v <path_to_repo>:/opt/vector-role -w /opt/vector-role -it aragast/netology:latest /bin/bash, где path_to_repo — путь до корня репозитория с vector-role на вашей файловой системе.

3.Внутри контейнера выполните команду tox, посмотрите на вывод.

4.Создайте облегчённый сценарий для molecule с драйвером molecule_podman. Проверьте его на исполнимость.

5.Пропишите правильную команду в tox.ini, чтобы запускался облегчённый сценарий.

6.Запустите команду tox. Убедитесь, что всё отработало успешно.

7.Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

8.После выполнения у вас должно получится два сценария molecule и один tox.ini файл в репозитории. Не забудьте указать в ответе теги решений Tox и Molecule заданий. В качестве решения пришлите ссылку на ваш репозиторий и скриншоты этапов выполнения задания.# 08-ansible-05-testing

### Скрины.
<img width="628" height="1023" alt="Скрин1(1)" src="https://github.com/user-attachments/assets/d9d598af-3357-4973-8b04-283e56f545c7" />
<img width="622" height="763" alt="Скрин1(2)" src="https://github.com/user-attachments/assets/011de769-4f08-4426-b424-33c81d0a87bb" />
<img width="491" height="478" alt="Скрин 2" src="https://github.com/user-attachments/assets/55f73d5c-4963-4532-aa4a-289deece3392" />
<img width="486" height="384" alt="Скрин3" src="https://github.com/user-attachments/assets/e3504dea-d884-4edb-a729-7bccc95acd37" />
<img width="514" height="758" alt="Скрин4(1)" src="https://github.com/user-attachments/assets/c1257f41-4149-4e8b-a64b-08bb7fa5e412" />
<img width="511" height="748" alt="Скрин4(2)" src="https://github.com/user-attachments/assets/9e5d8d69-5b6b-4667-af33-293f4bfb24dd" />
<img width="511" height="795" alt="Скрин4(3)" src="https://github.com/user-attachments/assets/0032849a-8d4c-478e-8479-4caff766fb07" />
<img width="512" height="793" alt="Скрин4(4)" src="https://github.com/user-attachments/assets/503b260a-6c7c-4b6d-8cee-31c343856b3f" />
<img width="520" height="575" alt="Скрин4(5)" src="https://github.com/user-attachments/assets/68cd9154-4b2c-4b5b-9868-c287d00737eb" />










