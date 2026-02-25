# DZ_Docker_Compose
# Домашнее задание к занятию 4 «Оркестрация группой Docker контейнеров на примере Docker Compose»

# Задача 1
https://hub.docker.com/r/lebedevrp/custom-nginx

# Задача 2

<img width="1376" height="420" alt="Задача 2" src="https://github.com/user-attachments/assets/8668ebf9-89d4-4a08-9a6e-57b2d3360b36" />

# Задача 3
![Задача 3 (подключиться к стандартному потоку ввода вывода ошибок)](https://github.com/user-attachments/assets/8b4ca527-e662-46c7-9404-97f98689df1c)
# Объяснение: Контейнер остановился, потому что при нажатии Ctrl+C во время docker attach сигнал SIGINT (прерывание) был передан главному процессу контейнера (nginx). Nginx, работающий в режиме "daemon off", получил сигнал завершения и остановился, что привело к остановке всего контейнера.
# Вход в интерактивный терминал контейнера. Установка текстового редактора
![Задача 3 (интерактивный терминал контейнера custom-nginx-t2 с оболочкой bash )](https://github.com/user-attachments/assets/6f17d13b-5d1d-4bf1-9ceb-1672b321a938)
# Редактирование конфигурации nginx, Перезагрузка nginx и проверка
![Задача 3 (замена порта с 80 на 81)](https://github.com/user-attachments/assets/ea44b6b6-1feb-48ad-b259-b94d013cb1ec)
# Проверка на хостовой машине
![Задача 3 (проверка на хосте)](https://github.com/user-attachments/assets/a55c3908-be99-465a-9652-7690cdea8242)
# Объяснение проблемы:
# Контейнер больше не отвечает на порту 8080, потому что:
# Мы изменили внутренний порт nginx с 80 на 81
# Проброс портов при запуске контейнера был настроен как 127.0.0.1:8080 -> 80
# Теперь nginx слушает порт 81 внутри контейнера, но хост продолжает отправлять трафик на порт 80 контейнера
# Удаление запущенного контейнера "custom-nginx-t2"
![Задача 3](https://github.com/user-attachments/assets/9714c90d-a6d1-43d3-8310-ffb642d936a8)

# Задача 4
![Задача 4](https://github.com/user-attachments/assets/5ffa2e92-a938-46ae-b38b-a77454126b15)

# Задача 5
# Согласно документации Docker Compose, по умолчанию при выполнении команды docker compose up ищутся файлы в следующем порядке: compose.yaml (предпочтительный), compose.yml, docker-compose.yaml, docker-compose.yml.Так как в директории присутствует compose.yaml, именно он и был использован.
<img width="896" height="429" alt="Задача 5" src="https://github.com/user-attachments/assets/ca861386-4a54-4e3d-97f2-e2eb334c6c5f" />
<img width="1231" height="500" alt="Задача 5 1" src="https://github.com/user-attachments/assets/4c989d22-6958-4d5e-8ba0-199b6529911f" />
<img width="924" height="621" alt="Задача 5 2" src="https://github.com/user-attachments/assets/fd6f00fa-0866-477c-b130-1ba6d35b3982" />










