```mermaid
architecture-beta
    group homelab[Home Lab]

    service internet(cloud)[Internet]
    service modem(internet)[Modem]
    service router(internet)[Router]
    service homegateway(server)[Home Gateway] in homelab
    service homecluster(server)[Home Cluster] in homelab

    junction junctionCenter in homelab

    internet:R -- L:modem
    modem:R -- L:router
    router:R -- L:junctionCenter
    junctionCenter:R -- L:homegateway
    junctionCenter:T -- L:homecluster
```
