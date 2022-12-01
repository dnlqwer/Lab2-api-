# Lab2-api-
## Поднятие сервера и организация доступа к нему: 
После поднятия REST сервера с моделью командой python -m deeppavlov riseapi squad_bert -p 1000 он будет запущен на 1000 порту хост-машины, но доступ будет только локальный по http://127.0.0.1:1000. 

Для получения доступа не только с хост-машины используем ngrok. В ngrok прописываем <code>ngrok.exe http 1000</code> получаем ссылку для подключения: https://514d-5-166-62-197.eu.ngrok.io.

### Работаем с сервером через командную строку.
<code>curl -X POST "https://514d-5-166-62-197.eu.ngrok.io/model" -H "accept: application/json" -H "Content-Type: application/json" 
-d "{\\"context_raw\\":[\\"Текст\\"], \\"question_raw\\":[\\"Вопрос\\"]}"</code>

 Пример: 
 curl -X POST "https://514d-5-166-62-197.eu.ngrok.io/model" -H "accept: application/json" -H "Content-Type: application/json" -d "{\"context_raw\":[\"DeepPavlov is a library for NLP and dialog systems.\"], \"question_raw\":[\"What is DeepPavlov?\"]}"
 
 Получаем следующий вывод: 
 
 

