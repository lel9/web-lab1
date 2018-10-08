# Лабораторная работа № 2
***

### Измерение скорости отдачи картинок:

 Параметр | без nginx | c nginx | gzip + cache
-|-----------|-----------|-----------|
Server Software | | nginx/1.14.0 | nginx/1.14.0 
Server Hostname | localhost | localhost | localhost 
Server Port | 8080 | 80 | 80 
Document Path | /img/test_image.jpeg | /img/test_image.jpeg | /img/test_image.jpeg
Document Length, bytes | 2059635 | 2059635 | 2059635
Concurrency Level | 10 | 10 | 10 
Time taken for tests, seconds | 0.934 | 0.201 | 0.240
Complete requests | 100 | 100 | 100
Failed requests | 0 | 0 | 0 |
Total transferred, bytes | 205991600 | 205987600 | 205987600
HTML transferred, bytes | 205963500 | 205963500 | 205963500
Requests per second [#/sec] (mean) | 107.06 | 498.56 | 416.61
Time per request [ms] (mean) | 93.406 | 20.058 | 24.003
Time per request [ms] (mean, across all concurrent requests) | 9.341 | 2.006 | 2.400
Transfer rate [Kbytes/sec] received | 215364.14 | 1002910.45 | 838050.46

### Измерение скорости отдачи html-cтраниц:

 Параметр | без nginx | c nginx | gzip + cache
-|-----------|-----------|-----------
Server Software | | nginx/1.14.0 | nginx/1.14.0
Server Hostname | localhost | localhost | localhost
Server Port | 8080 | 80 | 80
Document Path | /html/test_html.html  | /html/test_html.html  | /html/test_html.html
Document Length, bytes | 140 | 140 | 140
Concurrency Level | 10 | 10 | 10 
Time taken for tests, seconds | 0.092 | 0.038 | 0.028
Complete requests | 100 | 100 | 100 
Failed requests | 0 | 0 | 0
Total transferred, bytes | 42700 | 37200 | 37200
HTML transferred, bytes | 14000 | 14000 | 14000
Requests per second [#/sec] (mean) | 1081.19 | 2647.74 | 3522.99
Time per request [ms] (mean) | 9.249 | 3.777 | 2.839
Time per request [ms] (mean, across all concurrent requests) | 0.925 | 0.378 | 0.284
Transfer rate [Kbytes/sec] received | 450.85 | 961.88 | 1279.84

### Измерение скорости обработки POST запроса:

 Параметр | без nginx | c nginx | gzip + cache
-|-----------|-----------|-----------
Server Software | | nginx/1.14.0 | nginx/1.14.0
Server Hostname | localhost | localhost | localhost
Server Port | 8080 | 80 | 80
Document Path | /notes  | /notes | /notes
Document Length, bytes | 70 | 70 | 70
Concurrency Level | 10 | 10 | 10
Time taken for tests, seconds | 0.349 | 0.368 | 0.542
Complete requests | 100 | 100 | 100
Failed requests | 0 | 0 | 0
Total transferred, bytes | 27700 | 29900 | 29900
Total body sent | 22000 | 21800  21500
HTML transferred, bytes | 7000 | 7000 | 7000
Requests per second [#/sec] (mean) | 286.48 | 271.77 | 184.63
Time per request [ms] (mean) | 34.907 | 36.796 | 54.163
Time per request [ms] (mean, across all concurrent requests) | 3.491 | 3.680 | 5.416
Transfer rate [Kbytes/sec] received | 77.49 | 79.35 | 53.91
Transfer rate kb/s sent  | 61.55  | 57.86 | 38.76
Transfer rate kb/s total | 139.04 | 137.21 | 92.67

### Измерение скорости обработки GET запроса:

 Параметр | без nginx | c nginx | gzip + cache 
-|-----------|-----------|-------------
Server Software | | nginx/1.14.0 | nginx/1.14.0 
Server Hostname | localhost | localhost | localhost
Server Port | 8080 | 80 | 80
Document Path | /notes | /notes | /notes
Document Length, bytes | 42491 | 42491 | 21191
Concurrency Level | 10 | 10 | 10
Time taken for tests, seconds | 0.568 | 0.647 | 0.039
Complete requests | 100 | 100 | 100 
Failed requests | 0 | 0 | 0
Total transferred, bytes | 4270300 | 4272500 | 2142500
HTML transferred, bytes | 4249100 | 4249100 | 2119100
Requests per second [#/sec] (mean) | 176.06 | 154.45 | 2577.12
Time per request [ms] (mean) | 56.798 | 64.746 | 3.880
Time per request [ms] (mean, across all concurrent requests) | 5.680 | 6.475 | 0.388
Transfer rate [Kbytes/sec] received | 12550.77 | 7342.17 | 53920.71

Из полученных результатов измерения видно, что при использовании nginx скорость отдачи картинок увеличилась примерно в 2,5 раза, cкорость отдачи html страницы в 6,4 раза. Время обработки POST и GET запросов практически не изменилось. После настройки кеширования и gzip сжатия файлов, увеличилась скорость обработки GET запросов.
 
