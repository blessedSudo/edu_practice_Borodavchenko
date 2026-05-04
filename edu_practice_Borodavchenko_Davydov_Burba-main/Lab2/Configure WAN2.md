# Часть 1
## Шаг 1 - Создание топология сети

<img width="1597" height="543" alt="image" src="https://github.com/user-attachments/assets/fc5d9aac-e825-4470-95df-a5e86e175641" />

*Рис.1 Топология сети*

## Шаг 2 - Настройка интерфейсов f0/0 и f0/1 на маршрутизаторе R1

<img width="398" height="88" alt="image" src="https://github.com/user-attachments/assets/1661217b-a95a-4d3f-a684-e96940971412" />

*Рис.2 Настройка R1*

## Шаг 3 - Настройка интерфейсов f0/0 и f0/1 на маршрутизаторе R2

<img width="618" height="244" alt="image" src="https://github.com/user-attachments/assets/3a888568-4e81-4907-b815-5e505ef9332f" />

*Рис.3 Настройка R3*

## Шаг 4 - Настройка R3

<img width="631" height="422" alt="image" src="https://github.com/user-attachments/assets/e5584026-a715-4c0e-8825-5c8961295c94" />

*Рис.4 Настройка R4*

## Шаг 5 - Настройка R1973

<img width="575" height="154" alt="image" src="https://github.com/user-attachments/assets/5543dc63-fade-4fbf-94f5-0c6531e8a6b5" />

*Рис.5 Настройка R1973*

# Часть 2
## Шаг 1 - Настройка PPP на R3

<img width="598" height="143" alt="image" src="https://github.com/user-attachments/assets/8b161a69-7add-4257-9f12-27976b88b483" />

*Рис.6 Настройка PPP на R3*

## Шаг 2 - Настройка PPP на R1973

<img width="408" height="106" alt="image" src="https://github.com/user-attachments/assets/4d4d82b4-712e-4888-9b32-07f914f3ebd3" />

*Рис.7 Настройка PPP на R1973*

# Часть 3
## Шаг 1 - Настройка OSPFv2 на R1, R2, R3
R1:

<img width="200" height="23" alt="image" src="https://github.com/user-attachments/assets/2716b70f-1f97-43a0-bf51-0c2c6cc48bfd" />

*Рис.8 Настройка OSPFv2 на R1*

R2:

<img width="199" height="16" alt="image" src="https://github.com/user-attachments/assets/6f39f8a8-e992-4d7a-9d05-72f1177c9c19" />

*Рис.9 Настройка OSPFv2 на R2*

R3:

<img width="211" height="18" alt="image" src="https://github.com/user-attachments/assets/d5fc4f23-28f4-4fe1-bad5-8f893911cf2e" />

*Рис.10 Настройка OSPFv2 на R3*

## Шаг 2 - Router-id на R2

<img width="257" height="19" alt="image" src="https://github.com/user-attachments/assets/8bca3374-7d64-4911-af08-121bfaaa7f4c" />

*Рис.11 Настройка router-id на R2*

## Шаг 3 - Настройка объявлени всех подключений сети
R1:

<img width="384" height="29" alt="image" src="https://github.com/user-attachments/assets/2100fead-841d-4bbb-a681-122969003a3f" />

*Рис.12 настройка объявлений на R1*

R2:

<img width="410" height="34" alt="image" src="https://github.com/user-attachments/assets/4640cbe3-c05e-4339-86d4-0a911777599d" />

*Рис.13 настройка объявлений на R2*

R3:

<img width="428" height="49" alt="image" src="https://github.com/user-attachments/assets/17e87b1a-1820-4064-b2a2-d0eb14ea5976" />

*Рис.14 настройка объявлений на R3*

## Шаг 4 - Назначение f0/0 R1 в Area 1

<img width="377" height="20" alt="image" src="https://github.com/user-attachments/assets/adfe0ffc-fdfb-41e9-8de2-129a130fd726" />

*Рис.15 Назначение f0/0 R1 в Area 1*

## Шаг 5 - Назначение f0/1 R1 в Area 0

<img width="387" height="14" alt="image" src="https://github.com/user-attachments/assets/f315f8ab-fc45-4c72-bccb-f8db6286048f" />

*Рис.16 Назначение f0/1 R1 в Area 0*

## Шаг 6 - Назначение f0/0 R2 в Area 23

<img width="398" height="21" alt="image" src="https://github.com/user-attachments/assets/f54d059c-2e42-4ced-b2c6-c47c7162f152" />

*Рис.17 Назначение f0/0 R2 в Area 23*

## Шаг 7 - Назначение f0/1 R2 в Area 0

<img width="394" height="18" alt="image" src="https://github.com/user-attachments/assets/25fa237c-23af-4ea7-ac73-b9757b126b5a" />

*Рис.18 Назначение f0/1 R2 в Area 0*

## Шаг 8 - Назначение интерфейсов R3 в Area 23

<img width="426" height="44" alt="image" src="https://github.com/user-attachments/assets/061e354e-df86-4fc6-96fc-7fbc818dde74" />

*Рис.19  Назначение интерфейсов R3 в Area 23*

## Шаг 9 - Отключение hello-пакетов на R1, кроме f0/1

<img width="620" height="127" alt="image" src="https://github.com/user-attachments/assets/2fce8d37-5dbd-4901-8c2c-0babb7f36ca3" />

*Рис.20 Отключение hello-пакетов на R1*

## Шаг 10 - Настройка DR на R2

<img width="281" height="63" alt="image" src="https://github.com/user-attachments/assets/a5e7635e-12b2-4a26-b981-1c74b4a49190" />

*Рис.21 Настройка DR на R2*

## Шаг 11 - Назначение R3 шлюзом по умолчанию для OSPF

<img width="372" height="43" alt="image" src="https://github.com/user-attachments/assets/57b29383-d8db-4806-abbb-9c61e407f458" />

*Рис.22 Назначение R3 шлюзом по умолчанию для OSPF*

# Часть 4
## Шаг 1 - Настройка BGP

<img width="437" height="57" alt="изображение" src="https://github.com/user-attachments/assets/fe9d16b9-3bab-4ac1-816e-3a4897b55f75" />

*Рис.23 Заходим в BGP на R3*

<img width="228" height="35" alt="изображение" src="https://github.com/user-attachments/assets/e85c9382-66fb-437a-aa78-d36f53171cb7" />

*Рис.24 Заходим в BGP на R1973*

## Шаг 2 - Настраиваем соседство BGP 

<img width="401" height="16" alt="изображение" src="https://github.com/user-attachments/assets/6c39c360-f121-4975-8a39-fe0078252e13" />

*Рис.25 Добавляем соседство на R3*

<img width="470" height="30" alt="изображение" src="https://github.com/user-attachments/assets/2b22c7ad-b58c-4365-ac81-19ca0290c724" />

*Рис.26 Добавляем соседство на R1973*

## Шаг 3 - Объявляем loopback

<img width="418" height="15" alt="изображение" src="https://github.com/user-attachments/assets/9735afee-120b-4d90-8c51-f20cbe664ff6" />

*Рис.27 Добавляем loopback на R1973*

## Шаг 4 - Настройка маршрута по умолчанию

<img width="353" height="42" alt="изображение" src="https://github.com/user-attachments/assets/9515e671-6c57-49f9-9be2-7477791ff7cc" />

*Рис.28 Создаём маршрут по умолчанию на R1973*

## Шаг 5 - Проверка

<img width="572" height="211" alt="изображение" src="https://github.com/user-attachments/assets/a2945c7f-c6de-4451-88d4-f4129d7a7a17" />

*Рис.29 Проверка bgp*

# Часть 5
## Шаг 1 - Проверяем поддержку лицензии

<img width="491" height="302" alt="изображение" src="https://github.com/user-attachments/assets/53808926-e54f-42c2-961a-2edc932bc461" />

*Рис.30 Выполняем проверку на R3*

## Шаг 2 - Устанавливаем лицензию UCK9

<img width="470" height="19" alt="изображение" src="https://github.com/user-attachments/assets/7f9ede43-e1bc-4e60-b228-883296a570e9" />

*Рис.31 Установка лицензии*

<img width="619" height="129" alt="изображение" src="https://github.com/user-attachments/assets/7db4b336-5458-4a4b-a463-e455cf08f9b8" />

*Рис.32 После установочный вывод*

## Шаг 3 - Устанавливаем лицензию SecurityK9

<img width="486" height="21" alt="изображение" src="https://github.com/user-attachments/assets/2025625c-bad8-4894-a267-6c54c5f84d85" />

*Рис.33 Установка лицензии*

<img width="605" height="112" alt="изображение" src="https://github.com/user-attachments/assets/f97142ca-ca8d-41d8-8bc3-00730cefd73a" />

*Рис.34 После установочный вывод*

## Шаг 4 - Сохранение конфигурации

<img width="201" height="55" alt="изображение" src="https://github.com/user-attachments/assets/cd872b3d-db5c-493a-b089-0560a161283c" />

*Рис.35 Сохранение конфигурации*

## Шаг 5 - перезагружаем маршрутизатор

<img width="424" height="47" alt="изображение" src="https://github.com/user-attachments/assets/d5f28264-40ce-4c7d-ab72-bbf2b42805c0" />

*Рис.36 Перезагрузка маршрутизатора*

# Часть 6
## Шаг 1 - Настройка R1 в качестве DHCP-ретранслятора

<img width="432" height="91" alt="изображение" src="https://github.com/user-attachments/assets/6948cd09-4d35-4c1f-862f-b3cf95b3d75d" />

*Рис.37 Настройка R1*

## Шаг 2 - Проверка на PC0

<img width="692" height="305" alt="image" src="https://github.com/user-attachments/assets/428e8bf2-e5e8-45e0-9435-737e2d181bfe" />

*Рис.38 IP Configuration на PC0*

# Часть 7
## Шаг 1 - Настройка маршрутизаторов R1, R2, R3, R1973 с IPv6-адресами

<img width="446" height="171" alt="изображение" src="https://github.com/user-attachments/assets/6afc06e8-d8c9-4e1d-a797-ce1413ffa503" />

*Рис.39 Настройка IPv6 на R1*

<img width="445" height="134" alt="изображение" src="https://github.com/user-attachments/assets/3a0900f1-7cea-4030-aa96-eee06cd0405f" />

*Рис.40 Настройка IPv6 на R2*

<img width="445" height="121" alt="изображение" src="https://github.com/user-attachments/assets/a15796b9-9808-4841-baac-daab247abf63" />

*Рис.41 Настройка IPv6 на R3*

<img width="443" height="117" alt="изображение" src="https://github.com/user-attachments/assets/aa490ed6-7da0-4a17-ab1c-b2268b832479" />

*Рис.42 Настройка IPv6 на R1973*

## Шаг 2 - включение маршрутизации ipv6

<img width="229" height="16" alt="изображение" src="https://github.com/user-attachments/assets/b307b388-f2ff-4738-932f-a5f989f269c9" />

*Рис.43 Включение на R1*

<img width="252" height="13" alt="изображение" src="https://github.com/user-attachments/assets/9565498b-614b-4c17-a32b-637401f67e9a" />

*Рис.44 Включение на R2*

<img width="227" height="17" alt="изображение" src="https://github.com/user-attachments/assets/2752708d-ec5b-4a8d-8f66-22667c396ae3" />

*Рис.45 Включение на R3*

<img width="265" height="18" alt="изображение" src="https://github.com/user-attachments/assets/1d8199da-89cb-41fd-a59b-df355e5f2c4d" />

*Рис.46 Включение на R1973*

## Шаг 3 - Проверка f0/0 на R1

<img width="257" height="84" alt="изображение" src="https://github.com/user-attachments/assets/9f8d67ac-44d5-41c4-b1ef-3eaabbb292ee" />

*Рис.47 Проверка f0/0*

## Шаг 4 - Проверка использования EUI-64 на f0/0

<img width="393" height="142" alt="изображение" src="https://github.com/user-attachments/assets/90892dbe-c5cf-471f-8f13-2e4b86697ee2" />

*Рис.48 Проверка использования EUI-64 на f0/0*

# Часть 8

## Шаг 1 - Настройка OSPFv3

R1:

<img width="223" height="18" alt="изображение" src="https://github.com/user-attachments/assets/52cec44a-f4b9-4cc6-9127-46c4ac2b3282" />

*Рис.49 Настройка OSPFv3*

R2:

<img width="225" height="27" alt="изображение" src="https://github.com/user-attachments/assets/dacaca94-cf4b-4fc5-b511-ee01c5e3ebbd" />

*Рис.50 Настройка OSPFv3*

R3:

<img width="228" height="12" alt="изображение" src="https://github.com/user-attachments/assets/81d5e912-c875-49cc-9340-3b698cc8c6c9" />

*Рис.51 Настройка OSPFv3*

## Шаг 2 - Назначения Router-id

<img width="232" height="15" alt="изображение" src="https://github.com/user-attachments/assets/bfb0d02c-a0b9-45f0-9998-283b71d37924" />

*Рис.52 Назначение router-id на R1*

<img width="238" height="15" alt="изображение" src="https://github.com/user-attachments/assets/27f36f60-1126-42f5-9483-70d6885a9d0d" />

*Рис.53 Назначение router-id на R2*

<img width="238" height="16" alt="изображение" src="https://github.com/user-attachments/assets/b95f68b1-306a-48ea-8996-20daeefc1026" />

*Рис.54 Назначение router-id на R3*

## Шаг 3 - Настройка Area на R1

<img width="269" height="74" alt="изображение" src="https://github.com/user-attachments/assets/06ff3c6d-235b-490d-ba54-6f0267c2d7f0" />

*Рис.55 Настройка area на R1*

## Шаг 4 - Настройка area на R2

<img width="278" height="68" alt="изображение" src="https://github.com/user-attachments/assets/0190a1e2-e04d-475d-a86a-b3f43f44cae6" />

*Рис.56 Настройка area на R2*

## Шаг 5 - Настройка area на R3

<img width="254" height="28" alt="image" src="https://github.com/user-attachments/assets/4efeff7b-34fb-4d57-a611-70945ddfc911" />

*Рис.57 Настройка area на R3*

## Шаг 6 - Запрет на Hello-сообщения

<img width="607" height="141" alt="изображение" src="https://github.com/user-attachments/assets/ea99d59b-db85-4567-bdb8-2076542aab09" />

*Рис.58 Запрет Hello-сообщений на R1*

## Шаг 7 - Настройка R3 как шлюз по умолчанию

<img width="334" height="80" alt="изображение" src="https://github.com/user-attachments/assets/624f3776-352a-4cf8-b940-391eaf4de921" />

*Рис.59 Настройка R3 как шлюз по умолчанию*

<img width="581" height="59" alt="изображение" src="https://github.com/user-attachments/assets/d3db83ba-1029-43e5-ba93-aa3473a35cfe" />

*Рис.60 Проверка OSPFv3*

# Часть 9
## Шаг 1 - Настройка EIGRPv6 между R3 и R1973

<img width="442" height="46" alt="изображение" src="https://github.com/user-attachments/assets/f477c7d6-a603-45e1-b72f-572240b9ba17" />

*Рис.61 Настройка EIGRPv6 на R3*

<img width="437" height="44" alt="изображение" src="https://github.com/user-attachments/assets/500ca74c-d577-45e8-9976-a659edd869e8" />

*Рис.62 Настройка EIGRPv6 на R1973*

## Шаг 2 - Назначение router-id

<img width="276" height="34" alt="изображение" src="https://github.com/user-attachments/assets/14db794e-9311-4c19-b6a7-0afd94b57d14" />

*Рис.63 Назначение на R3*

<img width="300" height="27" alt="изображение" src="https://github.com/user-attachments/assets/f5773750-a589-4576-baf3-4084c18d479d" />

*Рис.64 Назначение на R1973*

## Шаг 3 - Объявление loopback 

<img width="243" height="71" alt="изображение" src="https://github.com/user-attachments/assets/243bfec2-7cf3-4d8d-9a46-85e0a3e31542" />

*Рис.65 Объявляем loopback на R1973*

<img width="209" height="31" alt="изображение" src="https://github.com/user-attachments/assets/e488abaa-abd6-47c2-a61e-1d6d7667d781" />

*Рис.66 Объявляем loopback на R3*

## Шаг 4 - Настройка ipv6 маршрут по умолчанию

<img width="346" height="17" alt="изображение" src="https://github.com/user-attachments/assets/fb11580b-9fe8-4053-b6ed-22cde60361c8" />

*Рис.67 Настраиваем на R1973*

<img width="547" height="100" alt="изображение" src="https://github.com/user-attachments/assets/86403f5a-cd39-4ee9-a4cc-11d0db6670b9" />

*Рис.68 Проверка на R3*

## Полная конфигурация

SW0:

```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch0
!
!
!
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

R1:

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
ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10175P9B-
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
interface FastEthernet0/0
 ip address 10.1.1.1 255.255.255.0
 ip helper-address 10.23.23.100
 duplex auto
 speed auto
 ipv6 address FE80::1 link-local
 ipv6 address 2001:10:10:10::/64 eui-64
 ipv6 ospf 100 area 1
!
interface FastEthernet0/1
 ip address 10.12.12.1 255.255.255.0
 duplex auto
 speed auto
 ipv6 address 2001:11:11:11::1/64
 ipv6 ospf 100 area 0
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 log-adjacency-changes
 passive-interface default
 no passive-interface FastEthernet0/1
 network 10.1.1.0 0.0.0.255 area 1
 network 10.12.12.0 0.0.0.255 area 0
!
ipv6 router ospf 100
 router-id 0.0.0.1
 log-adjacency-changes
 passive-interface default
 no passive-interface FastEthernet0/1
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
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```

R2:

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
!
!
!
!
!
ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10179225-
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
interface FastEthernet0/0
 ip address 10.23.23.2 255.255.255.0
 ip ospf priority 255
 duplex auto
 speed auto
 ipv6 address 2001:12:12:12::2/64
 ipv6 ospf 100 area 23
!
interface FastEthernet0/1
 ip address 10.12.12.2 255.255.255.0
 ip ospf priority 255
 duplex auto
 speed auto
 ipv6 address 2001:11:11:11::2/64
 ipv6 ospf 100 area 0
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 router-id 0.0.0.2
 log-adjacency-changes
 network 10.12.12.0 0.0.0.255 area 0
 network 10.23.23.0 0.0.0.255 area 23
!
ipv6 router ospf 100
 router-id 0.0.0.2
 log-adjacency-changes
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
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```

R3:

```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R3
!
!
!
!
!
!
!
!
no ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
username R1973 password 0 cisco
!
!
license udi pid CISCO2911/K9 sn FTX1524461N-
license boot module c2900 technology-package securityk9
license boot module c2900 technology-package uck9
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
interface Loopback3
 ip address 3.3.3.3 255.0.0.0
!
interface Loopback33
 ip address 33.33.33.33 255.0.0.0
!
interface GigabitEthernet0/0
 ip address 10.23.23.3 255.255.255.0
 duplex auto
 speed auto
 ipv6 address 2001:12:12:12::3/64
 ipv6 ospf 100 area 23
!
interface GigabitEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/2
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/0/0
 ip address 30.30.30.3 255.255.255.0
 encapsulation ppp
 ppp authentication chap
 ppp chap hostname R3
 ipv6 address 2001:30:30:30::3/64
 ipv6 eigrp 100
 clock rate 2000000
!
interface Serial0/0/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 log-adjacency-changes
 network 10.23.23.0 0.0.0.255 area 23
 network 3.0.0.0 0.255.255.255 area 23
 network 33.0.0.0 0.255.255.255 area 23
 default-information originate
!
router bgp 3
 bgp log-neighbor-changes
 no synchronization
 neighbor 30.30.30.73 remote-as 1973
!
ipv6 router ospf 100
 router-id 0.0.0.3
 default-information originate
 log-adjacency-changes
!
ipv6 router eigrp 100
 eigrp router-id 0.0.0.3
 no shutdown 
!
ip classless
ip route 0.0.0.0 0.0.0.0 30.30.30.73 
!
ip flow-export version 9
!
ipv6 route ::/0 2001:30:30:30::1973
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
end
```
R1973:

```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1973
!
!
!
!
!
!
!
!
no ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
username R3 password 0 cisco
!
!
license udi pid CISCO2911/K9 sn FTX152460B6-
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
interface Loopback1973
 ip address 73.73.73.73 255.255.255.0
 ipv6 address 2001:1973:1973:1973::1973/64
 ipv6 eigrp 100
!
interface GigabitEthernet0/0
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/2
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/0/0
 ip address 30.30.30.73 255.255.255.0
 encapsulation ppp
 ppp authentication chap
 ppp chap hostname R1973
 ipv6 address 2001:30:30:30::1973/64
 ipv6 eigrp 100
!
interface Serial0/0/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router bgp 1973
 bgp log-neighbor-changes
 no synchronization
 neighbor 30.30.30.3 remote-as 3
 network 73.73.73.0 mask 255.255.255.0
!
ipv6 router eigrp 100
 eigrp router-id 0.0.0.73
 no shutdown 
!
ip classless
ip route 0.0.0.0 0.0.0.0 30.30.30.3 
!
ip flow-export version 9
!
ipv6 route ::/0 2001:30:30:30::3
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
end
```

MLS:

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




