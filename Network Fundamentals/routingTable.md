```
Routing tables

Internet:
Destination        Gateway            Flags           Netif Expire 
default            homerouter.cpe     UGScg             en0
127                localhost          UCS               lo0
localhost          localhost          UH                lo0
169.254            link#14            UCS               en0      !
192.168.8          link#14            UCS               en0      !
192.168.8.1/32     link#14            UCS               en0      !
homerouter.cpe     88:40:3b:66:1c:eb  UHLWIir           en0   1190
d0-55-09-d3-69-c6  d0:55:9:d3:69:c6   UHLWI             en0   1130
192.168.8.188/32   link#14            UCS               en0      !
192.168.8.255      ff:ff:ff:ff:ff:ff  UHLWbI            en0      !
224.0.0/4          link#14            UmCS              en0      !
224.0.0.251        1:0:5e:0:0:fb      UHmLWI            en0
239.255.255.250    1:0:5e:7f:ff:fa    UHmLWI            en0
255.255.255.255/32 link#14            UCS               en0      !

Internet6:
Destination        Gateway            Flags           Netif Expire
default            fe80::%utun0       UGcIg           utun0
default            fe80::%utun1       UGcIg           utun1
default            fe80::%utun2       UGcIg           utun2
default            fe80::%utun3       UGcIg           utun3
default            fe80::%utun4       UGcIg           utun4
default            fe80::%utun5       UGcIg           utun5
default            fe80::%utun6       UGcIg           utun6
localhost          localhost          UHL               lo0
fd88:403b:661c:eb0 link#14            UC                en0
fd88:403b:661c:eb0 f8:4d:89:63:7c:60  UHL               lo0
fe80::%lo0         guohuijuandemacboo UcI               lo0
guohuijuandemacboo link#1             UHLI              lo0
fe80::%anpi2       link#4             UCI             anpi2
guohuijuandemacboo 1a:de:55:3e:f9:29  UHLI              lo0
fe80::%anpi1       link#5             UCI             anpi1
guohuijuandemacboo 1a:de:55:3e:f9:28  UHLI              lo0
fe80::%anpi0       link#6             UCI             anpi0
guohuijuandemacboo 1a:de:55:3e:f9:27  UHLI              lo0
fe80::%en0         link#14            UCI               en0
guohuijuandemacboo f8:4d:89:63:7c:60  UHLI              lo0
fe80::8a40:3bff:fe 88:40:3b:66:1c:eb  UHLWIi            en0
fe80::%awdl0       link#15            UCI             awdl0
fe80::48d6:83ff:fe 4a:d6:83:e6:c2:8f  UHLI              lo0
fe80::%llw0        link#16            UCI              llw0
fe80::48d6:83ff:fe 4a:d6:83:e6:c2:8f  UHLI              lo0
fe80::%utun0       guohuijuandemacboo UcI             utun0
guohuijuandemacboo link#18            UHLI              lo0
fe80::%utun1       guohuijuandemacboo UcI             utun1
guohuijuandemacboo link#19            UHLI              lo0
fe80::%utun2       guohuijuandemacboo UcI             utun2
guohuijuandemacboo link#20            UHLI              lo0
fe80::%utun3       guohuijuandemacboo UcI             utun3
guohuijuandemacboo link#21            UHLI              lo0
fe80::%utun4       guohuijuandemacboo UcI             utun4
guohuijuandemacboo link#22            UHLI              lo0
fe80::%utun5       guohuijuandemacboo UcI             utun5
guohuijuandemacboo link#23            UHLI              lo0
fe80::%utun6       guohuijuandemacboo UcI             utun6
guohuijuandemacboo link#24            UHLI              lo0
ff00::             localhost          UmCI              lo0
ff00::             link#4             UmCI            anpi2
ff00::             link#5             UmCI            anpi1
ff00::             link#6             UmCI            anpi0
ff00::             link#14            UmCI              en0
ff00::             link#15            UmCI            awdl0
ff00::             link#16            UmCI             llw0
ff00::             guohuijuandemacboo UmCI            utun0
ff00::             guohuijuandemacboo UmCI            utun1
ff00::             guohuijuandemacboo UmCI            utun2
ff00::             guohuijuandemacboo UmCI            utun3
ff00::             guohuijuandemacboo UmCI            utun4
ff00::             guohuijuandemacboo UmCI            utun5
ff00::             guohuijuandemacboo UmCI            utun6
ff01::%lo0         localhost          UmCI              lo0
ff01::%anpi2       link#4             UmCI            anpi2
ff01::%anpi1       link#5             UmCI            anpi1
ff01::%anpi0       link#6             UmCI            anpi0
ff01::%en0         link#14            UmCI              en0
ff01::%awdl0       link#15            UmCI            awdl0
ff01::%llw0        link#16            UmCI             llw0
ff01::%utun0       guohuijuandemacboo UmCI            utun0
ff01::%utun1       guohuijuandemacboo UmCI            utun1
ff01::%utun2       guohuijuandemacboo UmCI            utun2
ff01::%utun3       guohuijuandemacboo UmCI            utun3
ff01::%utun4       guohuijuandemacboo UmCI            utun4
ff01::%utun5       guohuijuandemacboo UmCI            utun5
ff01::%utun6       guohuijuandemacboo UmCI            utun6
ff02::%lo0         localhost          UmCI              lo0
ff02::%anpi2       link#4             UmCI            anpi2
ff02::%anpi1       link#5             UmCI            anpi1
ff02::%anpi0       link#6             UmCI            anpi0
ff02::%en0         link#14            UmCI              en0
ff02::%awdl0       link#15            UmCI            awdl0
ff02::%llw0        link#16            UmCI             llw0
ff02::%utun0       guohuijuandemacboo UmCI            utun0
ff02::%utun1       guohuijuandemacboo UmCI            utun1
ff02::%utun2       guohuijuandemacboo UmCI            utun2
ff02::%utun3       guohuijuandemacboo UmCI            utun3
ff02::%utun4       guohuijuandemacboo UmCI            utun4
ff02::%utun5       guohuijuandemacboo UmCI            utun5
ff02::%utun6       guohuijuandemacboo UmCI            utun6
ff15::efc0:988f    localhost          UHmW3I            lo0   3193
ff15::efc0:988f    link#4             UHmW3I          anpi2   3193
ff15::efc0:988f    link#5             UHmW3I          anpi1   3193
ff15::efc0:988f    link#6             UHmW3I          anpi0   3193
ff15::efc0:988f    guohuijuandemacboo UHmW3I          utun0   3193
ff15::efc0:988f    guohuijuandemacboo UHmW3I          utun1   3193
ff15::efc0:988f    guohuijuandemacboo UHmW3I          utun2   3193
ff15::efc0:988f    guohuijuandemacboo UHmW3I          utun3   3193
ff15::efc0:988f    guohuijuandemacboo UHmW3I          utun4   3193
ff15::efc0:988f    guohuijuandemacboo UHmW3I          utun5   3193
ff15::efc0:988f    guohuijuandemacboo UHmW3I          utun6   3193
```