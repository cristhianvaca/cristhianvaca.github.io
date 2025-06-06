---
layout: post
title:  "Route Distribution"
date:   2025-05-25 21:03:36 +0530
---
- La forma de configurar es :
    - Comandos de Configuración para redistribuir de OSPF A EIGRP

```jsx
router(config)# router eigrp ASN
router(config-router)# redistribute **SOURCE-PROTOCOL** [PID|ASN] [ metric BW[K]  DELAY[10u]  RELIABILITY LOAD MTU ][route-map MAP_NAME] // Metric in RD Command
router(config-router)# default-metric BW[K]  DELAY[10u]  RELIABILITY LOAD MTU   //Default-Metric Command

router(config)# router eigrp NAME
router(config-router)# address-family ipv4 unicast
router(config-router-af)# topology base
router(config-router-af-topology)# redistribute SOURCE-PROTOCOL [PID|ASN][ metric BW[K]  DELAY[10u]  RELIABILITY LOAD MTU ][route-map MAP_NAME]
router(config-router-af-topology)# default-metric BW[K]  DELAY[10u]  RELIABILITY LOAD MTU
```
