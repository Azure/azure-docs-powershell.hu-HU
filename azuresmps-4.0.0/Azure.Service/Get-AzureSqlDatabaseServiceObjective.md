---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015568"
---
# Get-AzureSqlDatabaseServiceObjective

## Áttekintés
Az Azure SQL adatbázis-kiszolgáló szolgáltatási céljainak beolvasása

## SZINTAXISA

### ByConnectionContext (alapértelmezett)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabaseServiceObjective** parancsmag az Azure SQL adatbázis-kiszolgáló szolgáltatási céljainak elérésére szolgál.
A szolgáltatási célkitűzéseket a teljesítmény szintjeként említik.
Ha nem ad meg szolgáltatási célkitűzést, ez a parancsmag visszaadja a megadott kiszolgáló érvényes szolgáltatási céljait.

Ez a parancsmag az alapszintű, a normál és a prémium szintű szolgáltatások szintjeire vonatkozik.

## Példák

### 1. példa: a szolgáltatás összes célkitűzésének beszerzése kapcsolati környezet használatával
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

Ez a parancs beilleszti a kiszolgáló összes olyan szolgáltatását, amelyre a kapcsolati környezet $Context adja meg.

### 2. példa: a szolgáltatás összes célkitűzésének beszerzése kiszolgálónév használatával
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

Ez a parancs a Server01 nevű kiszolgáló összes szolgáltatását megkapja.

## PARAMÉTEREK

### -Környezet
A kiszolgáló kapcsolati környezetét adja meg.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

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

### -ServiceObjective
Itt adhatja meg azt az objektumot, amely a parancsmag által beolvasott szolgáltatás célját jelképezi.
Az érvényes értékek a következők: 

- Alap: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) a legújabb SQL-adatbázis-frissítés V12 (előzetes verzió) része.
További információt az Azure [SQL Database V12 előzetes](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) verzió () újdonságai `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` Az Azure-tárban című témakörben talál.

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
A beszerzéshez használandó szolgáltatási cél nevét adja meg.
Az érvényes értékek: Basic, S0, S1, S2, S3, P1, P2 és P3.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. ServiceObjective

## KIMENETEK

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://msdn.microsoft.com/library/ee336279.aspx)

[A szolgáltatási szint elérési célja](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Új – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


