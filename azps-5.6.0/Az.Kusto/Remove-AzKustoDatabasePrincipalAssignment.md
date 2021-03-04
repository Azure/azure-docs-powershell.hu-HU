---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 66a5a844255f5a44000638877abf6a3ed5f908c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922377"
---
# Remove-AzKustoDatabasePrincipalAssignment

## SYNOPSIS
Egy Kusto principalAssignment törlése.

## SZINTAXIS

### Törlés (alapértelmezett)
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## LEÍRÁS
Egy Kusto principalAssignment törlése.

## PÉLDÁK

### 1. példa: Meglévő Kusto-adatbázis principalAssignment törlése név szerint
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

A fenti parancs törli a "kustoprincipal1" nevű PrincipalAssignment rekordot a Kusto-adatbázisban (mykustodatabase).

## PARAMETERS

### -AsJob
A parancs futtatása feladatként

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterName
A Kusto-fürt neve.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
A Kusto-fürtben található adatbázis neve.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
A parancs futtatása aszinkron módon

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Igaz értéket ad vissza, ha a parancs sikeres

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrincipalAssignmentName
A Kusto principalAssignment név.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A Kusto-fürtöt tartalmazó erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.
Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IKustoIdentity> Identity Parameter
  - `[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.
  - `[ClusterName <String>]`: A Kusto-fürt neve.
  - `[DataConnectionName <String>]`: Az adatkapcsolat neve.
  - `[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: Azure-hely.
  - `[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.
  - `[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.
  - `[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést. Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.

## KAPCSOLÓDÓ HIVATKOZÁSOK

