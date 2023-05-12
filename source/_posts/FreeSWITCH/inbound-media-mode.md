---
title: inbound 媒体处理模式
tags: FreeSWITCH
categories: media service
date: 2023.05.12
---

### sip_profiles/internal.xml

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<profile>
    <settings>
        <!--Uncomment to set all inbound calls to no media mode-->
        <!--<param name="inbound-bypass-media" value="true"/>-->

        <!--Uncomment to set all inbound calls to proxy media mode-->
        <!--<param name="inbound-proxy-media" value="true"/>-->

        <!-- Let calls hit the dialplan before selecting codec for the a-leg -->
        <param name="inbound-late-negotiation" value="true"/>
    </settings>
</profile>
```