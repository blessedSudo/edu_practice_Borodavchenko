
# Часть_1
## Шаг 1 - Схема сети
Создаём топологию сети, в которую входят 2 города
<img width="1935" height="692" alt="image" src="https://github.com/user-attachments/assets/ecfbfb7e-a4fd-4ffa-8da9-3291e4bca335" />
*Рис.1 топология сети*

## Шаг 2 - Создание сообщения на роутерах
rus-msk-r1: 

<img width="600" height="72" alt="image" src="https://github.com/user-attachments/assets/7e28204c-9dd1-48d8-b7cc-8d358283c6d5" />

*Рис.2 Настройка сообщения на первом роутере в Мск*

rus-msk-r2:

<img width="600" height="72" alt="image" src="https://github.com/user-attachments/assets/f4bd5894-1ea8-413e-80ef-781ebd90ec40" />

*Рис.3 Настройка сообщения на втором роутере в Мск*

rus-nsk-r1:

<img width="591" height="70" alt="image" src="https://github.com/user-attachments/assets/ae584d1b-d8d8-478d-9e32-d7501e2cc9be" />

*Рис.3 Настройка сообщения на первом роутере в Нск*

## Шаг 3 - Переименовывание устройств

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






