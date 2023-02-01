# torrent-vpn
mkdir -p transmission/data
mkdir -p transmission/config
mkdir -p transmission/transmission-data

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
