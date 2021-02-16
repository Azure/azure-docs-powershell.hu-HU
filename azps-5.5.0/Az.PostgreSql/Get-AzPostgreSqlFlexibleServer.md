---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: d8dc345ae9f307bbd5f1cd003edf1cba4a7ea6b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160394"
---
# Get-AzPostgreSqlFlexibleServer

## SYNOPSIS
Információkat kap a kiszolgálóról.

## SZINTAXIS

### Lista1 (alapértelmezett)
```
Get-AzPostgreSqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Lista
```
Get-AzPostgreSqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
Információkat kap a kiszolgálóról.

## PÉLDÁK

### 1. példa: A PostgreSql-kiszolgáló lekérte az alapértelmezett környezetben
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

Ez a parancsmag alapértelmezett környezetben kapja meg a PostgreSql-kiszolgálókat.

### 2. példa: A PostgreSql-kiszolgáló lekérte erőforráscsoport és kiszolgálónév szerint
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

Ez a parancsmag a PostgreSql-kiszolgálókat erőforráscsoport és kiszolgálónév szerint kapja meg.

### 3. példa: A megadott erőforráscsoport összes PostgreSql-kiszolgálója
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----             -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test  eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
postgresql-test2 eastus   postgresql-test     12     32768                   Standard_42s_v3 GeneralPurpose
```

Ez a parancsmag felsorolja a megadott erőforráscsoport összes PostgreSql-kiszolgálóját.

### 4. példa: A PostgreSql-kiszolgáló identitás alapján való lekérte
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Get-AzPostgreSqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test         12     32768                    Standard_D2s_v3 GeneralPurpose
```

Ez a parancsmaglista identitás alapján kapja meg a PostgreSql-kiszolgálókat.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A kiszolgáló neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.
A névben a kis- és

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A célként megcélzott előfizetés azonosítója.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IPostgreSqlIdentity> Identity Parameter
  - `[ConfigurationName <String>]`: A kiszolgáló konfigurációjának neve.
  - `[DatabaseName <String>]`: Az adatbázis neve.
  - `[FirewallRuleName <String>]`: A kiszolgáló tűzfalszabályának neve.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[LocationName <String>]`: A hely neve.
  - `[ResourceGroupName <String>]`: Az erőforráscsoport neve. A névben a kis- és
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: A biztonsági riasztási házirend neve.
  - `[ServerName <String>]`: A kiszolgáló neve.
  - `[SubscriptionId <String>]`: A cél-előfizetés azonosítója.
  - `[VirtualNetworkRuleName <String>]`: A virtuális hálózati szabály neve.

## KAPCSOLÓDÓ HIVATKOZÁSOK

