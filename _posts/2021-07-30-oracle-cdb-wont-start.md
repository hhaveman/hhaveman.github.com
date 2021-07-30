---
layout: post
title: "Oracle CDB won't start"
description: "Een database PDB wil is niet opgestart"
category:  [database]
tags: [database,oracle]
---
{% include JB/setup %}


Het kan gebeuren dat een de Oracle service wel opgestart is, maar dat pluggable
databases die in deze database zitten niet benaderbaar zijn.

Waarschijnlijk heeft de database zijn opstarten niet afgerond.

Om dit te verhelpen moet je in deze database inloggen als sysadmin.

```
sqlplus system/xxxx@//localhost:1521/pdbsid as sysdba
```

Vervolgens moet je even kijken naar de status van de database:

```
select status,database_status from v$instance;
```

Waarschijnlijk heeft de database de status **MOUNTED** terwijl hij de status
**OPEN** zou moeten hebben.

Zet de status op **OPEN**.

```
alter database open;
```

De database zou nu weer benaderbaar moeten zijn.

