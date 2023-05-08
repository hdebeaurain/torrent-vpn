Ce docker-compose permet de monter un tunnel VPN avec les providers disponibles [ici](https://haugene.github.io/docker-transmission-openvpn/supported-providers/) et d'y attacher un client web pour telecharger des torrents. Le connexion du conteneur du client provient du conteneur VPN. Si la connexion VPN se coupe, les deux images redemarreront et les telechargements de torrents reprendront une fois la connexion VPN retablie. 

# torrent-vpn
```bash
mkdir -p transmission/data && mkdir -p transmission/config && mkdir -p transmission/transmission-data && chmod -R 777 transmission
```

Il faut creer un fichier ".env" qui contiendra ces variables : 
```bash
# Transmission with OpenVPN
OPENVPN_PROVIDER=NORDVPN
OPENVPN_USERNAME=
OPENVPN_PASSWORD=
LOCAL_NETWORK=192.168.1.0/24
NORDVPN_PROTOCOL=TCP
NORDVPN_CATEGORY=P2P
NORDVPN_COUNTRY=Bulgaria

# Torrent client
```
Il est possible de changer le pays avec lequel etablir la connexion NordVPN, le nom du pays est a specifier dans le fichier *docker-compose.yml*. Le tableau se trouve en bas du README. 


Pour verifier si le conteneur se connecte bien au VPN :
```bash
curl ifconfig.me
```
Cela nous donne notre adresse IP publique
```bash
docker exec client-torrent curl --silent "http://ipinfo.io/ip"
```
Si cette IP est differente, le conteneur est bien connecte au VPN.

```

├── docker-compose.yml
├── README.md
├── **.env**
└── **transmission**
    ├── config
    │   ├── openvpn-credentials.txt
    │   └── transmission-home
    │       └── transmission.log
    └── **data**
        ├── incomplete
        └── **completed**

```


Country | Code | ID
--- | --- | ---
Albania | AL | 2
Argentina | AR | 10
Australia | AU | 13
Austria | AT | 14
Belgium | BE | 21
Bosnia and Herzegovina | BA | 27
Brazil | BR | 30
Bulgaria | BG | 33
Canada | CA | 38
Chile | CL | 43
Colombia | CO | 47
Costa Rica | CR | 52
Croatia | HR | 54
Cyprus | CY | 56
Czech Republic | CZ | 57
Denmark | DK | 58
Estonia | EE | 68
Finland | FI | 73
France | FR | 74
Georgia | GE | 80
Germany | DE | 81
Greece | GR | 84
Hong Kong | HK | 97
Hungary | HU | 98
Iceland | IS | 99
Indonesia | ID | 101
Ireland | IE | 104
Israel | IL | 105
Italy | IT | 106
Japan | JP | 108
Latvia | LV | 119
Lithuania | LT | 125
Luxembourg | LU | 126
Malaysia | MY | 131
Mexico | MX | 140
Moldova | MD | 142
Netherlands | NL | 153
New Zealand | NZ | 156
North Macedonia | MK | 128
Norway | NO | 163
Poland | PL | 174
Portugal | PT | 175
Romania | RO | 179
Serbia | RS | 192
Singapore | SG | 195
Slovakia | SK | 196
Slovenia | SI | 197
South Africa | ZA | 200
South Korea | KR | 114
Spain | ES | 202
Sweden | SE | 208
Switzerland | CH | 209
Taiwan | TW | 211
Thailand | TH | 214
Turkey | TR | 220
Ukraine | UA | 225
United Arab Emirates | AE | 226
United Kingdom | GB | 227
United States | US | 228
Vietnam | VN | 234
