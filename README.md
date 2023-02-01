# torrent-vpn
```
mkdir -p transmission/data && mkdir -p transmission/config && mkdir -p transmission/transmission-data
```

Il est possible de changer le pays avec lequel etablir la connexion NordVPN, le nom du pays est a specifier dans le fichier *docker-compose.yml* : 


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

```
docker-compose up -d
```

```

├── docker-compose.yml
├── README.md
└── **transmission**
    ├── **config**
    │   ├── openvpn-credentials.txt
    │   ├── transmission-credentials.txt
    │   └── transmission-home
    │       ├── blocklists
    │       ├── dht.dat
    │       ├── resume
    │       │   └── xx.torrent.xx.resume
    │       ├── settings.json
    │       ├── stats.json
    │       ├── torrents
    │       │   └── torrenthash.torrent
    │       └── transmission.log
    ├── **data**
    │   └── incomplete
    │       └── proxmox-ve_7.3-1.iso.part
    └── **transmission-data**
        ├── geoip
        │   ├── GeoLite2-City.mmdb
        │   └── GeoLite2-Country.mmdb
        ├── rtorrent
        │   ├── log
        │   │   └── rtorrent.log
        │   └── watch
        └── rutorrent
            ├── conf
            │   ├── access.ini
            │   ├── plugins.ini
            │   └── users
            ├── plugins
            ├── plugins-conf
            ├── rutorrent.log
            ├── share
            │   ├── torrents
            │   └── users
            └── themes

```
