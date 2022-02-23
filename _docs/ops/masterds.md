---
title: ACME-oPS As A Master Data Source
tags: 
 - ACME Master Data
 - API
 - SDK
description: ACME-oPS As A Master Data Source
---

# ACME-oPS as a Master Data Source 

{% include alert.html type="info" title="Content" content="About this option of ACME solution being a master data source." %}

{% include alert.html type="info" title="API docs links" content="The following API docs links would either have to open a dedicated page of this documentation (like they do now) or lead to an external API docs." %}

As an extended option, ACME-oPS can serve as a master data source **for keeping ‘golden’ records**. For that:
- ACME-oPS provides [an API for registering particular data types as maintained by ACME](api_data_reg). <br>
    After the type was registered, all data from different Services passing through the ACME-oPS contribute to the ‘golden’ records of objects of that type and kept locally in the Database provided by Customer
    - ACME supports PostgreSQL and MySQL as RDBMS for such persistence
- ACME-oPS provides [an API for managing master data](api_data_mng), i.e. ACME Types andACME Objects:
    - List of type descriptions can be retrieved, resulting in the list of ACME Types with IDs
    - ‘Golden’ records can be searched by a set of identifying attribute values, an ACME Object ID is returned
    - Objects can be retrieved by their ACME Object ID, type descriptions — by their ACME Type ID
    - Object attribute values can be changed
    - Object structure, i.e. an ACME Type structure, can be changed: attributes list or/and attribute names can be amended
- Whenever ACME Types or ACME Objects are changed, there should be calls to all relevant systems to notify them about the change. For that, ACME-oPS provides [interfaces (APIs) to register callbacks](api_clbk_reg) against ACME Type IDs or individual ACME Object IDs.
- ACME-oPS provides [interfaces (APIs)](api_mdata_clbk_dirmng) for and [SDK for directly manage](sdk_mdata_clbk_dirmng) all registered types, objects and callbacks
- ACME-CS provides [GUI for managing ACME Types](gui_types_mng). ACME Corp is hesitant to work with individual objects and callbacks just yet, so presently there’s no GUI for that.

>ACME-CS never directly interacts with ACME-oPS. Each communication is initiated solely by ACME-oPS. 