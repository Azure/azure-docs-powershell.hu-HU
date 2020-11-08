---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015570"
---
# Get-AzureSqlDatabaseServerQuota

## Áttekintés
Egy Azure SQL-adatbázis-kiszolgáló kvótájának adatait kapja meg.

## SZINTAXISA

### ByConnectionContext
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabaseServerQuota** parancsmag az Azure SQL Database Server adott példányához tartozó kvóta-információkat kapja meg.
Adja meg a kapcsolati környezetet vagy a kiszolgáló nevét.
Ha nem ad meg kvóta-nevet, ez a parancsmag a kiszolgáló összes kvóta-adatát kapja.

## Példák

### 1. példa: információk beszerzése adott kvótához
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

Ez a parancs az Premium_Databases nevű kvótát a $Context változóban tárolt kapcsolat által megadott Azure SQL adatbázis-kiszolgálóról kapja meg.

### 2. példa: információk kérése az összes kvótáról
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

Ez a parancs minden kvóta értékét a kapcsolat $Context által megadott kiszolgálóról kapja meg.

## PARAMÉTEREK

### -ConnectionContext
A kiszolgáló kapcsolati környezetét adja meg.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QuotaName
Megadja annak a kvóta-értéknek a nevét, amely a parancsmagot kapja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kiszolgálónév
A kiszolgáló nevét adja meg.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. ServerQuota []

## MEGJEGYZI
* Hitelesítés: Ez a parancsmag az SQL Server-hitelesítést vagy a tanúsítvány-alapú hitelesítést egyaránt használhatja. A hitelesítés beállításának példáit a New-AzureSqlDatabaseServerContext parancsmagban találhatja meg.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Új – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


