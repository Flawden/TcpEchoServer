# TcpEchoServer

Многопоточный TCP Echo Server по RFC 862: принимает данные от клиентов на порту 7 и отправляет их обратно.

## Как работает
- Слушает TCP порт 7 с помощью `ServerSocket`.  
- Для каждого подключения создаёт отдельный поток через `Thread`.  
- В каждом потоке читает входные данные (`BufferedReader`) и отправляет их обратно (`PrintWriter`).  
- Поддерживает параллельную обработку нескольких клиентов.  
- Закрытие соединения клиентом завершает соответствующий поток.

## Цель
- Отработка навыков многопоточности и сетевого программирования в Java.  
- Изучение работы с `ServerSocket` и `Socket` для TCP-соединений.  
- Реализация простого эхо-сервиса согласно стандарту RFC 862.
