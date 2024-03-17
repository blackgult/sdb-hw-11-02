# Домашнее задание к занятию «Кеширование Redis/memcached» - Михайлов Дмитрий


---

### Задание 1. Кеширование 

Приведите примеры проблем, которые может решить кеширование. 

*Приведите ответ в свободной форме.*

### Решение 1

Кеширование может решить следующие проблемы:
- Данные, к которым чаще всего обращаются, складываются в кэш для того, чтобы повысить производительность.
- При кэшировании уменьшается время ответа - следовательно, увеличивается скорость ответа.
- При кэшировании тяжелых запросов экономятся ресурсы базы данных.
- Использование кэширования во время резкой и/или пиковой нагрузки, например, на сайт, сглаживает резкое увеличение трафика (сглаживает резкое увеличение обращений пользователей к сайту) - из-за этого ускоряется загрузка сайта.

---

### Задание 2. Memcached

Установите и запустите memcached.

*Приведите скриншот systemctl status memcached, где будет видно, что memcached запущен.*

### Решение 2

![2-1](https://github.com/blackgult/sdb-hw-11-02/blob/main/2-1.PNG)

---

### Задание 3. Удаление по TTL в Memcached

Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5. 

*Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.*

### Решение 3

Вот что получалось у меня:

![3-3](https://github.com/blackgult/sdb-hw-11-02/blob/main/3-3.PNG)

Поскольку TTL в 5 секунд оказалось слишком мало, я увеличил TTL до 20 секунд.
Первый скриншот показывает, что я подключился через telnet, а второй скриншот (как продолжение первого) показывает два заданных мной ключа, которые через некоторое время "погибают".

Подлючился:

![3-1](https://github.com/blackgult/sdb-hw-11-02/blob/main/3-1.PNG)


Два моих ключа: key1 и key2

![3-2](https://github.com/blackgult/sdb-hw-11-02/blob/main/3-2.PNG)

---

### Задание 4. Запись данных в Redis

Запишите в Redis несколько ключей с любыми именами и значениями. 

*Через redis-cli достаньте все записанные ключи и значения из базы, приведите скриншот этой операции.*

### Решение 4

Поставил Redis, проверил его статус, что он запустился и добавил два ключа, а также достал все записанные ключи и значения.

![4-1](https://github.com/blackgult/sdb-hw-11-02/blob/main/4-1.PNG)

---
## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже разобраться в материале.

### Задание 5*. Работа с числами 

Запишите в Redis ключ key5 со значением типа "int" равным числу 5. Увеличьте его на 5, чтобы в итоге в значении лежало число 10.  

*Приведите скриншот, где будут проделаны все операции и будет видно, что значение key5 стало равно 10.*
