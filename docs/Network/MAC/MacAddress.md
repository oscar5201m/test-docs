# MAC Address

48-bit MACアドレスの構造

先頭 8 bits の中の、0番目と1番目の bit には意味がある。

<img
    src="../img/MAC-48_Address.png"
    alt="the structure of 48-bit MAC address"
    style="height: 400px; width: 400px;"
    onerror="this.onerror=null; this.src='./img/MAC-48_Address.png';"
/>

ref. [MAC address - Wikipedia](https://en.wikipedia.org/wiki/MAC_address)


| MACアドレスの例（抜粋） | 0番目 | 1番目 |
| --- | --- | --- |
| ``00:xx:xx:xx:xx:xx`` | ユニキャスト | グローバル |
| ``01:xx:xx:xx:xx:xx`` | マルチキャスト | グローバル |
| ``02:xx:xx:xx:xx:xx`` | ユニキャスト | ローカル |
| ``03:xx:xx:xx:xx:xx`` | マルチキャスト | ローカル |

<br>

他にも、予約済みの特殊なMACアドレスが「IEEE Standards Group MAC Addresses」の形でまとめられている。

ref. [IEEE Standard Group MAC Addresses](https://standards.ieee.org/products-programs/regauth/grpmac/public/)

| 特殊なMACアドレスの例（抜粋） | 使用用途 |
| --- | --- |
| ``ff:ff:ff:ff:ff:ff`` | ブロードキャスト |
| ``01:00:5e:xx:xx:xx`` | IPv4マルチキャスト用 |
| ``33:33:xx:xx:xx:xx`` | IPv6マルチキャスト用 |
| ``00:00:0c:07:ac:xx`` | HSRP (Hot Standby Router Protocol) 用 |
| ``00:00:5e:00:01:xx`` | VRRP (Virtual Router Redundancy Protocol) やCARP用 |
| ``01:00:0c:cc:cc:cc`` | Cisco CDP用 |
| ``01:80:c2:00:00:00`` | STP (Spanning Tree Protocol) 用 |
| ``01:80:c2:00:00:0e`` | LLDP (Link Layer Discovery Protocol) 用 |

