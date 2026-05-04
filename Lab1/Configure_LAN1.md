
# Часть 1
## Шаг 1 - Схема сети
Создаём топологию сети, в которую входят 2 города

<img width="1946" height="765" alt="image" src="https://github.com/user-attachments/assets/0091f8c8-ba45-4864-87f5-c86a030b886a" />

*Рис.1 топология сети*

## Шаг 2 - Создание сообщения на роутерах
rus-msk-r1: 

<img width="631" height="75" alt="image" src="https://github.com/user-attachments/assets/c0fa5cb7-6e29-493f-8245-526574e5350b" />

*Рис.2 Настройка сообщения на первом роутере в Мск*

rus-msk-r2:

<img width="631" height="75" alt="image" src="https://github.com/user-attachments/assets/642a47e4-ee76-46f9-9a15-1679613ac40b" />

*Рис.3 Настройка сообщения на втором роутере в Мск*

rus-nsk-r1:

<img width="631" height="75" alt="image" src="https://github.com/user-attachments/assets/7976c42f-7e57-4ffe-a20c-441b6b4aa339" />

*Рис.4 Настройка сообщения на первом роутере в Нск*

## Шаг 3 - Переименовывание устройств
#### Таблица названий устройств
<table>
<tr>
<td>

<h3>Москва</h3>
<table>
<tr><th>Первичная</th><th>Измененная</th></tr>
<tr><td>server0</td><td>rus-msk-serv1</td></tr>
<tr><td>switch0</td><td>rus-msk-sw1</td></tr>
<tr><td>router0</td><td>rus-msk-r1</td></tr>
<tr><td>router1</td><td>rus-msk-r2</td></tr>
<tr><td>Multilayer switch1</td><td>rus-msk-multisw1</td></tr>
<tr><td>PC0</td><td>rus-msk-pc6</td></tr>
<tr><td>PC1</td><td>rus-msk-pc7</td></tr>
</table>

</td>
<td>

<h3>Новосибирск</h3>
<table>
<tr><th>Первичная</th><th>Измененная</th></tr>
<tr><td>router0</td><td>rus-nsk-r1</td></tr>
<tr><td>switch0</td><td>rus-nsk-sw1</td></tr>
<tr><td>switch1</td><td>rus-nsk-sw2</td></tr>
<tr><td>PC0</td><td>rus-nsk-pc0</td></tr>
<tr><td>PC1</td><td>rus-nsk-pc1</td></tr>
<tr><td>PC2</td><td>rus-nsk-pc2</td></tr>
<tr><td>PC3</td><td>rus-nsk-pc3</td></tr>
<tr><td>PC4</td><td>rus-nsk-pc4</td></tr>
<tr><td>PC5</td><td>rus-nsk-pc5</td></tr>
</table>

</td>
</tr>
</table>

## Шаг 4 - Раздача доменных имён
rus-msk-sw1:

<img width="286" height="18" alt="image" src="https://github.com/user-attachments/assets/ea99f224-c1a2-43d5-beef-dad3a62c9987" />

*Рис.5 Назначение доменного имени*

rus-msk-r1:

<img width="448" height="72" alt="image" src="https://github.com/user-attachments/assets/f122e299-fa8b-4f14-8338-ba410862e69d" />

*Рис.6 Назначение доменного имени*

rus-msk-r2:

<img width="440" height="86" alt="image" src="https://github.com/user-attachments/assets/83007603-6cff-40d1-a5a3-952da141eda9" />

*Рис.7 Назначение доменного имени*

rus-nsk-r1:

<img width="255" height="15" alt="image" src="https://github.com/user-attachments/assets/27cc1aef-4ce3-44ab-a153-65b9439322f0" />

*Рис.8 Назначение доменного имени*

rus-nsk-sw1:

<img width="467" height="77" alt="image" src="https://github.com/user-attachments/assets/b674c8f3-f3d3-4416-938e-1c2bc6aedee8" />

*Рис.9 Назначеие доменного имени*

rus-nsk-sw2:

<img width="451" height="75" alt="image" src="https://github.com/user-attachments/assets/7ed0a68a-7483-4ff0-bd40-759af33412b1" />

*Рис10 Назначение доменного имени*

## Шаг 5 - Создание VLAN на коммутаторах в Нск

Создаём VLAN 2, 3, 4 на коммутаторах
rus-nsk-sw1:

<img width="182" height="88" alt="image" src="https://github.com/user-attachments/assets/6acaa5ce-5b4f-4acf-8011-8c0162c809a2" />

*Рис.11 Создание VLAN*

rus-nsk-sw2:

<img width="181" height="73" alt="image" src="https://github.com/user-attachments/assets/713dcc50-f7f6-45c9-be80-ae9edfa50ad3" />

*Рис.12 Создание VLAN*

## Шаг 6 - Назначение VLAN на интерфейсах

rus-nsk-sw1:

<img width="605" height="298" alt="image" src="https://github.com/user-attachments/assets/2a86a61c-46d0-43f2-abb7-f6a41631cd54" />

*Рис.13 Настройка VLAN на f0/2 и f0/3 на первом коммутаторе*

<img width="285" height="97" alt="image" src="https://github.com/user-attachments/assets/0928f4f9-2cfb-4510-972c-fd8874cba6b5" />

*Рис.14 Настройка VLAN на f0/4 на первом коммутаторе*

rus-nsk-sw2:

<img width="634" height="395" alt="image" src="https://github.com/user-attachments/assets/f689dc40-9b74-45b9-8181-823c992cc868" />

*Рис.15 Настройка VLAN на f0/2-4 на втором коммутаторе*

## Шаг 7 - Создание канала между коммутаторами в Нск

rus-nsk-sw1:

<img width="620" height="393" alt="image" src="https://github.com/user-attachments/assets/3e242da6-40a2-4b82-8ad5-4c92e58c4bd6" />

*Рис.16 настройка g0/1-2 на sw1*

rus-nsk-sw2:

<img width="614" height="368" alt="image" src="https://github.com/user-attachments/assets/e6b7a29c-7d36-434c-bdd4-affae5421aef" />

*Рис.17 настройка g0/1-2 на sw2*

## Шаг 8 - Создание Management interface на sw1 для VLAN 1

<img width="548" height="175" alt="image" src="https://github.com/user-attachments/assets/191eef49-f37c-4c6b-90a8-9d28cdd24faf" />

*Рис.18 Создание Management interface на sw1*

## Шаг 9 - Management interface на sw2 на VLAN 2

<img width="547" height="171" alt="image" src="https://github.com/user-attachments/assets/da398c89-b383-4731-8388-ff2f5c108d28" />

*Рис. 19 Создание Management interface на sw2*

## Шаг 10 - Включение SSHv2 на коммутаторах в Нск

rus-nsk-sw1:

<img width="617" height="381" alt="image" src="https://github.com/user-attachments/assets/6831f016-3daa-4c95-8a29-cea5516f684f" />

*Рис.20 Настройка на sw1*

rus-nsk-sw2:

<img width="619" height="269" alt="image" src="https://github.com/user-attachments/assets/bf4a6e32-f22a-4036-b814-e4ac7b9c87a5" />

*Рис.21 Настройка на sw2

## Шаг 11 - Настройка интерфейса f0/24 на SW1 к R1

<img width="458" height="87" alt="image" src="https://github.com/user-attachments/assets/d126e735-25a2-41ab-b562-e5f9fc5adbe7" />

*Рис.22 Настройка f0/24 на SW1*

## Шаг 12 - Настройка банера на SW1 и SW2 

<img width="688" height="141" alt="image" src="https://github.com/user-attachments/assets/62dada95-8ae5-41b1-b249-123d34b99091" />

*Рис.23 Настройка банера на SW1 и SW2*

## Шаг 13 - Настройка f0/2-4 на SW1 и SW2

rus-nsk-sw1:

<img width="649" height="521" alt="image" src="https://github.com/user-attachments/assets/c6003a6f-09b3-4295-b47c-97a7aec6771f" />

*Рис.24 Настройка интерфейсов на SW1*

rus-nsk-sw2:

<img width="654" height="478" alt="image" src="https://github.com/user-attachments/assets/d6ddba8d-f44c-45c4-83c9-1b9af52d0945" />

*Рис.25 Настройка интерфейсов на SW2*

## Шаг - 14 Защита консоли

<img width="254" height="172" alt="image" src="https://github.com/user-attachments/assets/f58ae33c-e97b-49fb-b447-629ee5c35b7d" />

*Рис.26 Защита консоли*

## Шаг 15 - Отключение таймаута 

<img width="693" height="254" alt="image" src="https://github.com/user-attachments/assets/9b3bd92b-a67b-44f6-8fb0-03dfc539d53d" />

*Рис.27 Отключение таймаута на коммутаторах*

## Шаг 16 - Отключение прерывания

<img width="692" height="257" alt="image" src="https://github.com/user-attachments/assets/2eb487b4-1338-42ea-86fb-d327f2bd4489" />

*Рис.28 Отключение прерывания на коммутаторах*

## Шаг 17 - Изменение размера буфера

<img width="665" height="161" alt="image" src="https://github.com/user-attachments/assets/3925e0e4-6632-4673-a038-81272e5a970c" />

*Рис.29 Изменение размера буфера на коммутаторах*

# Часть 2
## Шаг 1 - Назначение IP-адреса для F0/1 на R1

<img width="435" height="88" alt="image" src="https://github.com/user-attachments/assets/78ab74a7-435e-409f-93eb-4e642f518688" />

*Рис.30 Назначение IP-адреса для F0/1 на rus-nsk-r1*

## Шаг 2 - Настройка маршрутизации между VLAN 1, 2, 3, 4 на R1

<img width="437" height="311" alt="изображение" src="https://github.com/user-attachments/assets/058e079c-d625-4cf3-9447-7f7f02574c16" />

*Рис.31 Настройка R1 для маршрутизации между VLAN*

## Шаг 3 - Настройка R1 в качетсве DHCP-сервера

<img width="435" height="244" alt="изображение" src="https://github.com/user-attachments/assets/8a796154-e4a6-4bb8-ae4a-c79f316c77bb" />

*Рис.32 исключение пула адресов*

<img width="306" height="295" alt="изображение" src="https://github.com/user-attachments/assets/d79276dc-f005-40f3-8200-c30bfd408b00" />

*Рис.33 Создание пула адресов для VLAN*

## Шаг 4 - Проверка настройки 

<img width="418" height="195" alt="изображение" src="https://github.com/user-attachments/assets/14f337b0-9b75-4336-a379-1e574ec0d39d" />

*Рис.34 Проверка настройки с помощью пинга*

# Часть 3

## Шаг 1 - Настройка имени хоста Multilayer Switch

<img width="446" height="72" alt="изображение" src="https://github.com/user-attachments/assets/7eab1223-a0de-4933-832f-42974aa6fa07" />

*Рис.35 Присваивание имени хоста Multilayer Switch*

## Шаг 2 - Включение возможности маршрутизации на MLS

<img width="172" height="17" alt="изображение" src="https://github.com/user-attachments/assets/93e9be50-08c7-4aef-b080-4af4fe43fa42" />

*Рис.36 Включение маршрутизации

## Шаг 3 - Создание VLAN 100 и VLAN 200 и присваивание имени

<img width="253" height="70" alt="изображение" src="https://github.com/user-attachments/assets/76e941a2-e7de-4a21-ad1c-0fc060f639f2" />

*Рис.37 Создание VLAN 100 и 200 и присваивание имени*

## Шаг 4 - Назначение VLAN для f0/4 и f0/5

<img width="297" height="207" alt="изображение" src="https://github.com/user-attachments/assets/26e2f6b0-7673-497e-9cbf-828f996b0173" />

*Рис.38 Назначение VLAN для интерфейсов*

## Шаг 5 - Включение маршрутизации между VLAN

<img width="558" height="223" alt="изображение" src="https://github.com/user-attachments/assets/960f293b-3df2-4414-8587-222236c4c80a" />

*Рис.39 Включение маршрутизации между VLAN*

## Шаг 6 - Изменение интерфейсов f0/1-3

<img width="615" height="282" alt="изображение" src="https://github.com/user-attachments/assets/cb6c6192-5156-4efb-9c1c-51d1de0fd6a8" />

*Рис.40 Изменение интерфейсов f0/1-3*

## Шаг 7 - Проверка

<img width="407" height="186" alt="изображение" src="https://github.com/user-attachments/assets/457f7780-b6c5-4981-9f85-074966c79a99" />

*Рис.41 Проверка настройки пингом*

# Часть 4
## Шаг 1 - Настройка интерфейсов f0/0 и f0/1 на R1 в Москве

<img width="320" height="85" alt="изображение" src="https://github.com/user-attachments/assets/49b46e54-e551-42ca-a9b3-d4d9cd29e7b9" />

*Рис.42 Настройка интерфейсво на R1*

## Шаг 2 - Настройка интерфейсов f0/0 и f0/1 на R2 в Москве

<img width="443" height="143" alt="изображение" src="https://github.com/user-attachments/assets/ad88b408-a126-406e-991a-65f5b17b1a18" />

*Рис.43 Настройка интерфейсво на R2*

## Шаг 3 - Настройка Cisco High availability на R1 и R2

rus-msk-r1:

<img width="335" height="132" alt="изображение" src="https://github.com/user-attachments/assets/75f84dd2-460f-43d0-b0d2-461a6cf0fe2f" />

*Рис.44  Настройка Cisco High availability на R1*

rus-msk-r2:

<img width="267" height="57" alt="изображение" src="https://github.com/user-attachments/assets/1d29a985-1c37-47d6-bc65-3c9143d2c55d" />

*Рис. 45 Настройка Cisco High availability на R2*

# Часть 5
## Шаг 1 - Настройка EIGRP
rus-nsk-r1:

<img width="335" height="101" alt="изображение" src="https://github.com/user-attachments/assets/f681d454-9015-431b-97a6-3228db5a4e04" />

*Рис.46 настройка EIGRP на R1 в Нск*

rus-msk-r1:

<img width="354" height="57" alt="изображение" src="https://github.com/user-attachments/assets/aca5177d-c4ee-4b26-a14b-489cca772f7b" />

*Рис.47 настройка EIGRP на R1 в Москве*

rus-msk-r2:

<img width="353" height="43" alt="изображение" src="https://github.com/user-attachments/assets/e35341a3-cc36-462b-b4b9-399d0a62a151" />

*Рис.48 настройка EIGRP на R2 в Москве*

rus-msk-multisw1:

<img width="623" height="248" alt="изображение" src="https://github.com/user-attachments/assets/114e32a7-aed1-4f04-be47-3a8c03883683" />

*Рис.49 настройка EIGRP на multisw1*

## Шаг 2 - Проверка с помощью SSH

Подключение SSH с сервера на sw1:

<img width="182" height="102" alt="изображение" src="https://github.com/user-attachments/assets/e6e1d816-a440-4dd5-b3c4-9ee41d7d9915" />

*Рис.50 SSH на sw1*

Подключение SSH с сервера на sw2:

<img width="188" height="99" alt="изображение" src="https://github.com/user-attachments/assets/319a37dc-620c-40d6-992a-e67bc180034c" />

*Рис.51 SSH на sw2*

## Шаг 3 - Пинг с сервера:

<img width="402" height="189" alt="изображение" src="https://github.com/user-attachments/assets/39b707e5-ed4f-4911-b0e0-b1de627e194a" />

*Рис.52 Пинг с сервера*

# Часть 6
## Шаг 1 - Настройка доступа по SSH к SW1 и SW2 

rus-nsk-sw1:

<img width="440" height="146" alt="изображение" src="https://github.com/user-attachments/assets/5c18d549-6261-4796-85db-0550b9b8148b" />

*Рис.53 Настройка доступа SSH на sw1*

rus-nsk-sw2:

<img width="425" height="115" alt="изображение" src="https://github.com/user-attachments/assets/02f8707b-c7b7-4a9b-926e-de0e2727e6cf" />

*Рис.54 Настройка доступа SSH на sw2*

## Шаг 2 - Настройка доступ к веб-серверу

rus-nsk-r1:

<img width="572" height="98" alt="изображение" src="https://github.com/user-attachments/assets/03300c19-87a6-4546-ab17-53205b1bbe46" />

*Рис.55 Настройка доступ к веб-серверу*

## Шаг 3 - Запрет ответа на ping R1 и R2 в Москве

rus-msk-r1:

<img width="416" height="126" alt="изображение" src="https://github.com/user-attachments/assets/d5e76c66-2fca-4bb2-bb5f-8e997260c189" />

*Рис.56 Запрет ответа на ping на R1*

rus-msk-r2:

<img width="485" height="144" alt="изображение" src="https://github.com/user-attachments/assets/be52bbf0-c337-402d-926e-6ecd59ac41f0" />

*Рис.57 Запрет ответа на ping на R2*

# Часть 7
## Шаг 1 - Создание loopback-интерфейса на R1

rus-nsk-r1:

<img width="573" height="114" alt="изображение" src="https://github.com/user-attachments/assets/28fdf07f-2fac-4ae0-b922-61ca01df7ade" />

*Рис.58 Создание loopback-интерфейса на R1*

## Шаг 2 - Настройка loopback на R2 в Москве

rus-msk-r2:

<img width="556" height="114" alt="изображение" src="https://github.com/user-attachments/assets/d04073c8-8ffa-48d3-aa6a-7bfe273c4373" />

*Рис.59 Настройка loopback на R2*

## Шаг 3 - Настройка анонсирования Loopback-интерфейса через RIPv2

rus-nsk-r1:

<img width="307" height="72" alt="изображение" src="https://github.com/user-attachments/assets/02a80a80-5852-424d-8a3b-6d18cf23abc1" />

*Рис.60 Настройка анонсирования loopback-интерфейса*

rus-msk-r2:

<img width="295" height="72" alt="изображение" src="https://github.com/user-attachments/assets/cb62b348-75c1-4f89-afcb-afd490eedcd0" />

*Рис.61 Настройка анонсирования loopback-интерфейса*

## Шаг 4 - Ограничение работы RIPv2

rus-msk-r1:

<img width="185" height="14" alt="изображение" src="https://github.com/user-attachments/assets/2edd2ba1-54ca-4a38-b05c-43dac06f6bef" />

*Рис.62 Ограничение RIPv2 на R1 в Мск*

rus-msk-multisw1:

<img width="193" height="17" alt="изображение" src="https://github.com/user-attachments/assets/6ba769e5-8270-4230-88c4-4e110365baf7" />

*Рис.63 Ограничение RIPv2 на MLS в Мск*

## Шаг 5 - Настройка IP-адресации туннеля 

rus-nsk-r1:

<img width="566" height="143" alt="изображение" src="https://github.com/user-attachments/assets/a7eca41c-7834-48d8-9eed-3ad37fa57a69" />

*Рис.64 Настройка IP-адресации туннеля на R1*

rus-msk-r2:

<img width="554" height="143" alt="изображение" src="https://github.com/user-attachments/assets/9d63a710-5e64-4685-98fb-c633f942c6dd" />

*Рис.65 Настройка IP-адресации туннеля на R2*

## Шаг 6 - Проверка

<img width="510" height="343" alt="изображение" src="https://github.com/user-attachments/assets/1a4ecfe0-e66e-4f6d-a217-8201506d4760" />

*Рис.66 Проверка loopback-интерфейса*

# Часть 8
## Шаг 1 - Настрйока NTP-сервера и Syslog-сервера
rus-nsk-r1:

<img width="436" height="98" alt="image" src="https://github.com/user-attachments/assets/2e35a392-ac1b-4c45-bc8d-c5c8f555379d" />

*Рис.67 Настрйока NTP-сервера и Syslog-сервера*


rus-msk-r1:

<img width="452" height="116" alt="image" src="https://github.com/user-attachments/assets/c5524641-e2e4-4707-ba70-fc937cd2c8f4" />

*Рис.68 Настрйока NTP-сервера и Syslog-сервера*

rus-msk-r2:

<img width="440" height="99" alt="image" src="https://github.com/user-attachments/assets/02070ecd-e981-4e15-8960-c5c0abe1c01b" />

*Рис.69 Настрйока NTP-сервера и Syslog-сервера*

## Шаг 2 - Включение SNMP на R1 и R2 в Мск
rus-msk-r1:

<img width="500" height="49" alt="image" src="https://github.com/user-attachments/assets/d6a55e92-bdb4-47f1-ade8-acbfe6fec285" />

*Рис.70 Включение SNMP на R1 в Мск*

rus-msk-r2

<img width="486" height="49" alt="image" src="https://github.com/user-attachments/assets/b967ce1f-0a48-4038-bdae-e2cb1224e6dd" />

*Рис.71 Включение SNMP на R2 в Мск*

## Шаг 3 - Настройка AAA и Telnet на R2 в Мск
rus-msk-r2:

<img width="474" height="86" alt="image" src="https://github.com/user-attachments/assets/5e737d71-5061-4ac3-9955-6fdf6753de32" />

*Рис.72 Настройка AAA и Telnet на R2 в Мск*

## Шаг 4 - Настройка FTP на R1 в Мск
rus-msk-r1:

<img width="232" height="33" alt="image" src="https://github.com/user-attachments/assets/977e5b21-31a5-471c-be40-bd6bccaeafb3" />

*Рис.72 Настройка FTP на R1 в Мск*

## Шаг 5 - Отправка конфигурации R1 на сервер, с помощью FTP
rus-msk-r1:

<img width="358" height="116" alt="image" src="https://github.com/user-attachments/assets/e31a6014-bbf1-438e-9926-8c6ad9327e0e" />

*Рис.73 Отправка конфигурации*

## Шаг 6 - Отправка конфигурации R2 на сервер, с помощью TFTP
rus-msk-r2:

<img width="339" height="116" alt="image" src="https://github.com/user-attachments/assets/f2ae31fa-3df8-43db-b80d-655b0efe158e" />

*Рис.74 Отправка конфигурации*

## Шаг 7 - Проверка на использование команд boot system в R2 в Мск
rus-msk-r2:

<img width="200" height="27" alt="image" src="https://github.com/user-attachments/assets/55ee8688-8341-4a7b-b7cf-8b07188edd3c" />

*Рис.75 Проверка на использование команд boot system в R2 в Мск*

Команда ничего не выдаёт, значит команд boot system нет

## Шаг 8 - Проверка подключения к R2 в Мск по telnet
Для начала создадим пользователя Standby на R2.

rus-msk-r2:

<img width="308" height="18" alt="image" src="https://github.com/user-attachments/assets/13809c60-4791-4cce-a7d5-44b5a6a0ad34" />

*Рис.76 Создание пользователя Standby*

Для работы на R2 по telnet нужео поставить пароль для перехода в привилегерованный режим.

rus-msk-r2:

<img width="233" height="16" alt="image" src="https://github.com/user-attachments/assets/e94b7ef9-c161-4e19-ad11-2950ebbf0d2e" />

*Рис.77 Пароль для привилегерованного режима.*

Дальше можем подключаться по telnet.

rus-msk-r1:

<img width="611" height="159" alt="image" src="https://github.com/user-attachments/assets/a16d6036-3c5d-4bfd-a271-d7514d707042" />

*Рис.78 Подключение к R2 по telnet*

## Шаг 9 - Изменение локального имени пользователя в R2
Для начала вводим команду для игнорирования конфигурации при загрузке. Вся настройка происходит на rus-msk-r2.

<img width="195" height="35" alt="image" src="https://github.com/user-attachments/assets/76202214-a736-4576-ba0b-512e57d4ddc1" />

*Рис.79 Ввод команды для игнорирования конфигурации при загрузке.*

Дальше предложит войти в диалоговое окно начальнйо настойки, нужно отказаться.

<img width="531" height="20" alt="image" src="https://github.com/user-attachments/assets/f4deac0f-50e0-42bf-a942-b4a7360d01d5" />

*Рис.80 Отказ от входа в диалоговое окно начальной настройки*

Затем загружаем старую конфигурацию и изменяем имя пользователя 

<img width="639" height="243" alt="image" src="https://github.com/user-attachments/assets/4362e2a0-10ad-4a8e-b0b2-e5ffe290e6a8" />

*Рис.81 загрузка старой конфигурации

Возвращаем значение конфигурационного регистра.

<img width="242" height="20" alt="image" src="https://github.com/user-attachments/assets/80cd64a1-1723-4984-97d4-ea201ca975ea" />

*Рис.82 Возвращение значения конфигурационного регистра.

# Полная конфигурация устройств
rus-msk-r1
```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1
!
!
!
!
!
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10173D5Q-
!
!
!
!
!
!
!
!
!
ip ftp username cisco
ip ftp password cisco
ip domain-name msk.local
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 10.0.0.2 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
 standby 1 ip 10.0.0.1
 standby 1 preempt
 standby 1 track FastEthernet0/1
!
interface FastEthernet0/1
 ip address 11.0.0.2 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
 network 11.0.0.0
!
ip classless
!
ip flow-export version 9
!
!
access-list 120 permit icmp any any echo-reply
access-list 120 deny icmp any any echo
access-list 120 permit ip any any
!
banner motd #Rabotu vypolnili Borodavchenko Daniil, Davydov Matvey, Burba Ulyana studenty gruppy 9SA-321, v zhurnale pod nomerami 5, 6, 8!#
!
!
!
snmp-server community cisco RW
!
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```
rus-msk-r2:
```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R2
!
!
!
enable secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
!
!
aaa new-model
!
aaa authentication login TELNET_AUTH group radius local 
!
!
!
!
!
!
!
no ip cef
no ipv6 cef
!
!
!
username newadmin secret 5 $1$mERr$y1xCpu9vTanV1oFENCDrX0
username standby secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
license udi pid CISCO2811/K9 sn FTX10177M0D-
!
!
!
!
!
!
!
!
!
ip domain-name msk.local
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface Loopback0
 ip address 192.168.103.3 255.255.255.0
!
interface Tunnel0
 ip address 200.200.200.3 255.255.255.0
 mtu 1476
 tunnel source FastEthernet0/0
 tunnel destination 40.40.40.1
!
!
interface FastEthernet0/0
 ip address 10.0.0.3 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
 standby 1 ip 10.0.0.1
 standby 1 preempt
!
interface FastEthernet0/1
 ip address 12.0.0.3 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
 network 12.0.0.0
!
router rip
 version 2
 network 192.168.103.0
 network 200.200.200.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
!
access-list 120 permit icmp any any echo-reply
access-list 120 deny icmp any any echo
access-list 120 permit ip any any
!
banner motd #Rabotu vypolnili Borodavchenko Daniil, Davydov Matvey, Burba Ulyana studenty gruppy 9SA-321, v zhurnale pod nomerami 5, 6, 8!#
!
radius server 10.0.0.100
 address ipv4 10.0.0.100 auth-port 1645
 key cisco
!
!
snmp-server community cisco RW
!
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login authentication TELNET_AUTH
 transport input telnet
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```
rus-msk-sw1:
```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SW1
!
!
!
ip domain-name msk.local
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
!
interface FastEthernet0/2
!
interface FastEthernet0/3
!
interface FastEthernet0/4
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
!
!
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
!
!
!
end
```
rus-msk-multisw1:
```
!
version 12.2(37)SE1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname MLS
!
!
!
!
!
!
ip routing
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/1
 no switchport
 ip address 11.0.0.50 255.0.0.0
 duplex auto
 speed auto
!
interface FastEthernet0/2
 no switchport
 ip address 12.0.0.50 255.0.0.0
 duplex auto
 speed auto
!
interface FastEthernet0/3
 no switchport
 ip address 40.40.40.50 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/4
 switchport access vlan 100
 switchport mode access
!
interface FastEthernet0/5
 switchport access vlan 200
 switchport mode access
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
interface Vlan100
 mac-address 000c.cf1e.8501
 ip address 100.0.0.50 255.0.0.0
!
interface Vlan200
 mac-address 000c.cf1e.8502
 ip address 200.0.0.50 255.255.255.0
!
router eigrp 100
 network 11.0.0.0
 network 12.0.0.0
 network 40.40.40.0 0.0.0.255
 network 100.0.0.0
 network 200.0.0.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
!
end

```
rus-nsk-r1:
```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1
!
!
!
!
ip dhcp excluded-address 1.0.0.1 1.0.0.99
ip dhcp excluded-address 1.0.0.201 1.0.0.254
ip dhcp excluded-address 2.0.0.1 2.0.0.99
ip dhcp excluded-address 2.0.0.201 2.0.0.254
ip dhcp excluded-address 3.0.0.1 3.0.0.99
ip dhcp excluded-address 3.0.0.201 3.0.0.254
ip dhcp excluded-address 4.0.0.1 4.0.0.99
ip dhcp excluded-address 4.0.0.201 4.0.0.254
!
ip dhcp pool VLAN1
 network 1.0.0.0 255.0.0.0
 default-router 1.0.0.1
 dns-server 8.8.8.8
ip dhcp pool VLAN2
 network 2.0.0.0 255.0.0.0
 default-router 2.0.0.1
 dns-server 8.8.8.8
ip dhcp pool VLAN3
 network 3.0.0.0 255.0.0.0
 default-router 3.0.0.1
 dns-server 8.8.8.8
ip dhcp pool VLAN4
 network 4.0.0.0 255.0.0.0
 default-router 4.0.0.1
 dns-server 8.8.8.8
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017ZTUG-
!
!
!
!
!
!
!
!
!
ip domain-name nsk.local
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface Loopback0
 ip address 192.168.101.1 255.255.255.0
!
interface Tunnel0
 ip address 200.200.200.1 255.255.255.0
 mtu 1476
 tunnel source FastEthernet0/1
 tunnel destination 10.0.0.3
!
!
interface FastEthernet0/0
 no ip address
 duplex auto
 speed auto
!
interface FastEthernet0/0.1
 encapsulation dot1Q 1 native
 ip address 1.0.0.1 255.0.0.0
!
interface FastEthernet0/0.2
 encapsulation dot1Q 2
 ip address 2.0.0.1 255.0.0.0
 ip access-group 110 in
!
interface FastEthernet0/0.3
 encapsulation dot1Q 3
 ip address 3.0.0.1 255.0.0.0
!
interface FastEthernet0/0.4
 encapsulation dot1Q 4
 ip address 4.0.0.1 255.0.0.0
!
interface FastEthernet0/1
 ip address 40.40.40.1 255.255.255.0
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 1.0.0.0
 network 2.0.0.0
 network 3.0.0.0
 network 4.0.0.0
 network 40.40.40.0 0.0.0.255
!
router rip
 version 2
 network 192.168.101.0
 network 200.200.200.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
!
access-list 110 permit tcp host 2.0.0.100 host 10.0.0.100 eq www
access-list 110 deny tcp 2.0.0.0 0.255.255.255 host 10.0.0.100 eq www
access-list 110 permit ip any any
!
banner motd #Rabotu vypolnili Borodavchenko Daniil, Davydov Matvey, Burba Ulyana studenty gruppy 9SA-321, v zhurnale pod nomerami 5, 6, 8!#
!
!
!
!
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```
rus-nsk-sw1:
```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SW1
!
!
!
ip ssh version 2
ip domain-name nsk.local
!
username nsk secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Port-channel1
 switchport mode trunk
!
interface FastEthernet0/1
!
interface FastEthernet0/2
 switchport access vlan 2
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/3
 switchport access vlan 3
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/4
 switchport access vlan 4
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
 switchport mode trunk
!
interface GigabitEthernet0/1
 switchport mode trunk
 channel-group 1 mode active
!
interface GigabitEthernet0/2
 switchport mode trunk
 channel-group 1 mode active
!
interface Vlan1
 ip address 1.0.0.50 255.0.0.0
!
ip default-gateway 1.0.0.1
!
banner motd #Eto rus-nsk-sw1#
!
!
!
access-list 10 permit host 10.0.0.100
access-list 10 permit host 2.0.0.100
line con 0
 logging synchronous
 login local
 history size 256
 exec-timeout 0 0
!
line vty 0 4
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
line vty 5 15
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
!
!
!
!
end
```
rus-nsk-sw2:
```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SW2
!
!
!
ip ssh version 2
ip domain-name nsk.local
!
username nsk secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Port-channel1
 switchport mode trunk
!
interface FastEthernet0/1
 shutdown
!
interface FastEthernet0/2
 switchport access vlan 2
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/3
 switchport access vlan 3
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/4
 switchport access vlan 4
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
 switchport mode trunk
 channel-group 1 mode passive
!
interface GigabitEthernet0/2
 switchport mode trunk
 channel-group 1 mode passive
!
interface Vlan1
 no ip address
 shutdown
!
interface Vlan2
 ip address 2.0.0.50 255.0.0.0
!
ip default-gateway 2.0.0.1
!
banner motd #Eto rus-nsk-sw2#
!
!
!
access-list 10 permit host 10.0.0.100
access-list 10 permit host 2.0.0.100
line con 0
 logging synchronous
 login local
 history size 256
 exec-timeout 0 0
!
line vty 0 4
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
line vty 5 15
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
!
!
!
!
end
```
rus-msk-serv1:

<img width="690" height="424" alt="image" src="https://github.com/user-attachments/assets/d8cac5cb-6825-4469-a5dc-2ce40eb6735c" />

*Рис.83 IP-конфигурация сервера*

rus-msk-pc6:

<img width="686" height="476" alt="image" src="https://github.com/user-attachments/assets/9ba36e70-dc3e-432c-b70d-44021b406d84" />

*Рис.84 IP-конфигурация пк6*

rus-msk-pc7:

<img width="697" height="451" alt="image" src="https://github.com/user-attachments/assets/c7f0e88f-b92b-47d4-8a5f-9c8316e3d9a8" />

*Рис.85 IP-конфигурция пк7*

rus-nsk-pc0:

<img width="685" height="447" alt="image" src="https://github.com/user-attachments/assets/102da92f-bbc7-4cae-88d9-73fafc3d1c18" />

*Рис.86 IP-конфигурация пк0*

rus-nsk-pc1:

<img width="692" height="445" alt="image" src="https://github.com/user-attachments/assets/7a1b9748-52a6-4a7f-9dc8-43f0d00d5667" />

*Рис.87 IP-конфигурация пк1*

rus-nsk-pc2:

<img width="694" height="450" alt="image" src="https://github.com/user-attachments/assets/d4c7455a-8745-4f20-a181-e35b227e024e" />

*Рис.88 IP-конфигурация пк2*

rus-nsk-pc3:

<img width="698" height="318" alt="image" src="https://github.com/user-attachments/assets/173b0026-8b5e-4b6e-96a3-34452075d1c7" />

*Рис.89 IP-конфигурация пк3*

rus-nsk-pc4:

<img width="694" height="449" alt="image" src="https://github.com/user-attachments/assets/2cb44686-cf06-4b46-9923-a39867b2b374" />

*Рис.90 IP-конфигурация пк4

rus-nsk-pc5:

<img width="699" height="461" alt="image" src="https://github.com/user-attachments/assets/58c652ce-5cc5-4f5c-b293-9f949f181707" />

*Рис.91 IP-конфигурация пк5*























































































