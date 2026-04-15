
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
