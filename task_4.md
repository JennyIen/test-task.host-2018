**_Задание 4:_** *В приведенном ниже тексте исправьте 	допущенные синтаксические, орфографические, 	грамматические ошибки. При необходимости 	поправьте стилистику и оформление 	текста.*

**_Оригинальный текст_**

Состояние сети находится в крайне плачевном состояниии требует не только работ, связанных с настройкой и модернизацией оборудования, но и общей реструктризацией сети, документированием и актуализацией информации по всей сетевой инфраструктуре.
Сеть в целом - не управляемая, что приводит к значительному увеличению времени диагностики при неисправности сети.
Безопасность сети не отвечает элементарным требованиям, а именно:
	- Разграничение 	сети компании и гостевой сети;
	- Вывод 	серверов, имеющих внешние подключении 	в DMZ;
	- Ограничение 	доступа к интерфейсам управления 	оборудования.
В качестве основного провайдера используется ISP, но по качеству предоставляемых услуг он годится, разве лишь, для домашних пользователей. Так как имеет существеные недостатки при использовании безлемитного доступа:
	- Число 	одновременных сессий может быть 	ограничено провайдером;
	- Абонент 	должен использовать защищенное 	соединение VPNлибо 	пользоваться авторизатором;
	- Скорость 	доступа к сети интернет не является 	гарантированной;
	- Подключение 	осуществляется только на один ipадрес.
Для доступа в интернет используется два провайдера, что правильно, но не настроена балансировка исходящих соединений и при отказе основного провайдера необходимо вручную переключать канал доступа в интернет. Так время простоя может быть существенным и зависит от скорости реагирования системным администратором либо лицом его заменяющим.
Использование оборудования разных вендоров в целом приемлемо, но в будущем возможны ситуации тяжелой совместимости устройств разных вендоров (сложности с агрегацией каналов, проблемы с протоколом STP, трудности настройки транкинга).

Рекомендации
Необходимо телекоммуникационную стойку привести в порядок. Все патчкорды промаркировать и уложить в коробы.
В целях предотвращения отказов сети в случае кратковременого пропадания электричества, необходимо все телекоммуникационное оборудование подключить к источнику бесперебойного питания.
Необходимо разделить все по разным группам VLAN и ограничить доступ к VLAN интерфейсов управления оборудованием.
В целях обеспечения безопасности необходимо гостевую точку доступа Wi-Fi подключить непосредственно к провайдеру услуг интернет без транзита трафика через локальную сеть компании. Для этого можно использовать имеющуюся в наличии точку доступаLynkSysWRT54G2, так в ней есть необходимый сервис DHCP.
Для обеспечения лучшей безопасности необходимо использовать два Firewall. Организовать DMZ и вывести туда все серверы, к которым есть подключения из сети интернет
Для более оптимального использования каналов интернет необходимо перевести тариф на безлимитный и настроить балансировку нагрузки на оба канала. Так же при этом будет достигнуто автоматическое перенаправление трафика при падение какого либо одного канала доступа в интернет.


**_Исправленный текст_**

### Отчет о состоянии сети
Сеть требует серьезных доработок. Необходимо провести работы, связанные с настройкой сети и модернизацией оборудования. Также требуется общая реструктуризация, документирование и актуализация информации по всей сетевой инфраструктуре.

Сетью, по факту, никто не управляет. Это приводит к увеличению времени диагностики неисправностей.


Состояние сети не отвечает следующим требованиям информационной безопасности:

- Разграничение внутренней сети компании и гостевой сети;

- Вывод в DMZ серверов с Интернет-сервисами;

- Ограничение доступа к интерфейсам управления оборудованием.


Основной Интернет-провайдер для сети, “IPS”, не соответствует рабочим требованиям. Также предоставляемые “IPS” услуги имеют следующие недостатки:

- Число одновременных соединений с Интернет может быть ограничено провайдером;

- Для подключения к сети Интернет необходимо использовать VPN или авторизатор;

- Скорость доступа к сети Интернет не гарантирована;

- Подключение осуществляется только на один IP-адрес.


Для доступа в интернет используется два провайдера, но отказоустойчивость исходящего соединения не настроена: при отказе основного провайдера необходимо вручную переключаться на другого провайдера. Время простоя зависит от скорости реагирования системного администратора.

Допустимо использовать оборудование разных поставщиков, но в будущем могут возникнуть ситуации несовместимости: сложности с агрегацией каналов, проблемы с протоколом STP, трудности настройки транкинга.

### Рекомендации
1. Необходимо привести в порядок телекоммуникационную стойку: промаркировать и уложить в короба все соединительные кабеля.
2. Все телекоммуникационное оборудование нужно подключить к источнику бесперебойного питания, чтобы предотвратить отказ сети в случае кратковременного отсутствия электричества.
3. Необходимо распределить все по разным VLAN и ограничить доступ к VLAN для всех интерфейсов управления оборудованием.
4. Гостевую сеть Wi-Fi необходимо подключить к провайдеру услуг Интернет без транзита трафика через локальную сеть компании. Для этого можно использовать имеющуюся точку доступа LynkSys WRT54G2, так как в ней есть необходимый для работы гостевой сети сервис DHCP.
5. Для обеспечения большей безопасности, необходимо использовать два раздельных Firewall. А также создать DMZ и вывести туда все серверы, к которым есть подключения из сети Интернет.
6. Для оптимального использования каналов сети Интернет, необходимо перейти на безлимитный тариф и настроить отказоустойчивость и балансировку нагрузки на оба канала. Тогда перенаправление трафика при падении одного из каналов будет происходить автоматически.