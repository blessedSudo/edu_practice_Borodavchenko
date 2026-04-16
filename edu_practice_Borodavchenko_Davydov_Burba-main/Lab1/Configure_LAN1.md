
# Часть 1
## Шаг 1 - Схема сети
Создаём топологию сети, в которую входят 2 города
<img width="1947" height="760" alt="image" src="https://github.com/user-attachments/assets/b97ffbdf-ba91-46ad-8949-521aaada4637" />
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
<tr><td>PC0</td><td>rus-msk-pc1</td></tr>
<tr><td>PC1</td><td>rus-msk-pc2</td></tr>
</table>

</td>
<td>

<h3>Новосибирск</h3>
<table>
<tr><th>Первичная</th><th>Измененная</th></tr>
<tr><td>router0</td><td>rus-nsk-r1</td></tr>
<tr><td>switch0</td><td>rus-nsk-sw1</td></tr>
<tr><td>switch1</td><td>rus-nsk-sw2</td></tr>
<tr><td>PC0</td><td>rus-nsk-pc1</td></tr>
<tr><td>PC1</td><td>rus-nsk-pc2</td></tr>
<tr><td>PC2</td><td>rus-nsk-pc3</td></tr>
<tr><td>PC3</td><td>rus-nsk-pc4</td></tr>
<tr><td>PC4</td><td>rus-nsk-pc5</td></tr>
<tr><td>PC5</td><td>rus-nsk-pc6</td></tr>
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

















