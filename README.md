# Домашнее задание к занятию "`10.2 Кластеризация`" - `Вахрамеев А.В.`



### Задание 1. 

В чем различие между SMP и MPP системами?

*Приведите ответ в свободной форме.*

---


SMP (symmetric multiprocessing) – симметричная многопроцессорная архитектура. Главной особенностью систем с архитектурой SMP является наличие общей физической памяти, разделяемой всеми процессорами.

MPP (massive parallel processing) – массивно-параллельная архитектура. Главная особенность такой архитектуры состоит в том, что память физически разделена. В этом случае система строится из отдельных модулей, содержащих процессор, локальный банк операционной памяти (ОП), коммуникационные процессоры (рутеры) или сетевые адаптеры, иногда – жесткие диски и/или другие устройства ввода/вывода.


---

### Задание 2.

В чем отличие сильно связанных и слабо связанных систем?

*Приведите ответ в свободной форме.*

---

В слабо связанных системах вся память распределена между процессорными элементами. Пример таких систем:●системы с массовым параллелизмом (MPP), кластерные системы.

Сильно связанная система состоит из нескольких однородных процессоров и массива общей памяти (обычно из нескольких независимых блоков). Представители таких систем: ●SMP (cимметричные мультипроцессоры),●NUMA (системы с неоднородным доступом к памяти).

---

### Задание 3.

Какие преимущества отличают кластерные системы от обычных серверов?

*Приведите ответ в свободной форме.*

---


абсолютная масштабируемость,

нет ограничений на размер узлов и кластеров,

наращиваемая масштабируемость,

можно расширять узлы по необходимости,

высокий коэффициент готовности,

отказоустойчивость, благодаря автономности узлов,

соотношение цена/производительность,

можно строить кластер из любых строительных блоков: чем проще и стандартнее блоки, тем дешевле обходится вычислительная мощность.

---

### Задание 4.

Приведите примеры типов современных кластерных систем?

*Приведите ответ в свободной форме.*

---

отказоустойчивые кластеры (High-availability clusters, HA, кластеры высокой доступности);

кластеры с балансировкой нагрузки (Load balancing clusters);

вычислительные кластеры (High performance computing clusters, HPC);

системы распределенных вычислений.

---

### Задание 5.

Где использует сервис Kafka, rabitMQ?

*Приведите ответ в свободной форме.*

---

Kafka Apache — распределенная система обмена сообщениями между серверными приложениями в режиме реального времени. Благодаря высокой пропускной способности, масштабируемости и надежности применяется в компаниях, работающих с большими объемами данных.

Kafka Apache — эффективный инструмент для организации работы серверных проектов любого уровня. Благодаря гибкости, масштабируемости и отказоустойчивости используется в различных направлениях IT-индустрии, от сервисов потоковых видео до аналитики Big Data.

Для связи микросервисов. Kafka — связующее звено между отдельными функциональными модулями большой системы. Например, с ее помощью можно подписать микросервис на другие компоненты для регулярного получения обновлений.
Потоковая передача данных. Высокая пропускная способность системы позволяет поддерживать непрерывные потоки информации. За счет грамотной маршрутизации «Кафка» не только надежно передает данные, но и позволяет производить с ними различные операции.
Ведение журнала событий. Kafka сохраняет данные в строго организованную структуру, в которой всегда можно отследить, когда произошло то или иное событие. Информация хранится в течение заданного промежутка времени, что можно использовать для разгрузки базы данных или медленно работающих систем логирования. 

RabbitMQ — распределённый и горизонтально масштабируемый брокер сообщений. Упрощённо его устройство можно описать так:

паблишер, который отправляет сообщения;

очередь, где хранятся сообщения;

подписчики, которые выступают получателями сообщений.

RabbitMQ передаёт сообщения между поставщиками и подписчиками через очереди. Сообщения могут содержать любую информацию, например, о событии, произошедшем на сайте. 

RabbitMQ отлично подходит для интеграции разных компонентов, создания микросервисов, потоковой передачи данных в режиме реального времени или при передаче работы удалённым работникам. Его используют крупные компании, в числе которых Bloomberg, Reddit, WeWork, NASA и др. 

Почему выбирают RabbitMQ:

RabbitMQ поддерживает несколько протоколов: AMQP, MQTT, STOMP и др., что позволяет использовать его в разных сценариях.

RabbitMQ хранит сообщение до тех пор, пока принимающее приложение не подключится и не получит его из очереди. Клиент может подтвердить получение сообщения сразу или после того, как полностью обработает его. Как только такое подтверждение получено, сообщение удаляется из очереди. Для сравнения в Kafka очередь сообщений является постоянной — данные хранятся, пока не истечёт указанный период или не будет достигнуто ограничение по размеру. Поэтому важно убедиться, что событие, которое должно произойти один раз, не воспроизводится многократно. 

Основное преимущество RabbitMQ — гибкая маршрутизация. Сообщения маршрутизируются через exchange (обменник) перед попаданием в очереди. RabbitMQ предлагает несколько встроенных типов обмена для типичной логики маршрутизации. 

RabbitMQ поддерживает приоритезацию в очередях и позволяет настроить диапазон приоритетов. Приоритет каждого сообщения устанавливается при его публикации. 

RabbitMQ предлагает простой пользовательский интерфейс управления. Он позволяет контролировать каждый аспект брокера сообщений. .

---
