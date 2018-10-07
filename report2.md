# Лабораторная работа № 2
***

Измерение скорости отдачи картинок:

 Параметр | без nginx | c nginx |
-|-----------|-----------|
Server Software | | nginx/1.14.0 |
Server Hostname | localhost | localhost |
Server Port | 8080 | 80 |
Document Path | /img/image.png | /img/image.png |
Document Length, bytes | 594459 | 594459 |
Concurrency Level | 10 | 10 |
Time taken for tests, seconds | 0.379 | 0.150 |
Complete requests | 100 | 100 |
Failed requests | 0 | 0 |
Total transferred, bytes | 59473700 | 59469700 |
HTML transferred, bytes | 59445900 | 59445900 |
Requests per second [#/sec] (mean) | 263.63 | 666.51 |
Time per request [ms] (mean) | 37.932 | 15.004 |
Time per request [ms] (mean, across all concurrent requests) | 3.793 | 1.500 |
Transfer rate [Kbytes/sec] received | 153116.75 | 387079.63 |

Измерение скорости отдачи html-cтраниц:

 Параметр | без nginx | c nginx |
-|-----------|-----------|
Server Software | | nginx/1.14.0 |
Server Hostname | localhost | localhost |
Server Port | 8080 | 80 |
Document Path | /html/index.html  | /html/index.html  |
Document Length, bytes | 79 | 79 |
Concurrency Level | 10 | 10 |
Time taken for tests, seconds | 0.221 | 0.034 |
Complete requests | 100 | 100 |
Failed requests | 0 | 0 |
Total transferred, bytes | 36500 | 31000 |
HTML transferred, bytes | 7900 | 7900 |
Requests per second [#/sec] (mean) | 451.68 | 2909.43 |
Time per request [ms] (mean) | 22.140 | 3.437 |
Time per request [ms] (mean, across all concurrent requests) | 2.214 | 0.344 |
Transfer rate [Kbytes/sec] received | 161.00 | 880.78 |

Измерение скорости обработки POST запроса:

 Параметр | без nginx | c nginx |
-|-----------|-----------|
Server Software | | nginx/1.14.0 |
Server Hostname | localhost | localhost |
Server Port | 8080 | 80 |
Document Path | /notes  | /notes |
Document Length, bytes | 70 | 70 |
Concurrency Level | 10 | 10 |
Time taken for tests, seconds | 0.427 | 0.475 |
Complete requests | 100 | 100 |
Failed requests | 0 | 0 |
Total transferred, bytes | 27700 | 29900 |
Total body sent | 22000 | 21500 |
HTML transferred, bytes | 7000 | 7000 |
Requests per second [#/sec] (mean) | 234.24 | 210.71 |
Time per request [ms] (mean) | 42.692 | 47.458 |
Time per request [ms] (mean, across all concurrent requests) | 2.214 | 4.746 |
Transfer rate [Kbytes/sec] received | 63.36 | 61.53 |
Transfer rate kb/s sent  | 50.32  | 44.24 |
Transfer rate kb/s total | 113.69 | 105.77 |

Измерение скорости обработки GET запроса:

 Параметр | без nginx | c nginx |
-|-----------|-----------|
Server Software | | nginx/1.14.0 |
Server Hostname | localhost | localhost |
Server Port | 8080 | 80 |
Document Path | /notes | /notes |
Document Length, bytes | 83291 | 83291 |
Concurrency Level | 10 | 10 |
Time taken for tests, seconds | 0.650 | 0.737 |
Complete requests | 100 | 100 |
Failed requests | 0 | 0 |
Total transferred, bytes | 8350400 | 8352600 |
HTML transferred, bytes | 8329100 | 8329100 |
Requests per second [#/sec] (mean) | 153.91 | 135.71 |
Time per request [ms] (mean) | 64.974 | 73.684 |
Time per request [ms] (mean, across all concurrent requests) | 6.497 | 7.368 |
Transfer rate [Kbytes/sec] received | 12550.77 | 11069.98 |


Из полученных результатов измерения видно, что при использовании nginx скорость отдачи картинок увеличилась примерно в 2,5 раза, cкорость отдачи html страницы в 6,4 раза. Время обработки POST и GET запросов практически не изменилось.
 
