---
title: acl 配置
tags: FreeSWITCH
categories: media service
date: 2023.05.12
---

### 案例1：警告信息

```shell
[WARNING] switch_core_media.c:4173 NO candidate ACL defined, Defaulting to wan.auto
```

### 案例1：修改 sip_profiles/external.xml 和 sip_profiles/internal.xml

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<profile>
    <settings>
        <!-- 添加配置 -->
        <param name="apply-candidate-acl" value="wan"/>
        <param name="apply-candidate-acl" value="localnet.auto"/>
        <param name="apply-candidate-acl" value="rfc1918.auto"/>
    </settings>
</profile>
```

