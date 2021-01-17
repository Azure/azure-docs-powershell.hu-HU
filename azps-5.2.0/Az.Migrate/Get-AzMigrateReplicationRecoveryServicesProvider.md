---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369947"
---
# Get-AzMigrateReplicationRecoveryServicesProvider

## SYNOPSIS
A regisztrált helyreállítási szolgáltató adatait tartalmazza.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## LEÍRÁS
A regisztrált helyreállítási szolgáltató adatait tartalmazza.

## PÉLDÁK

### 1. példa: Az összes szolgáltató behozatkja a tárolóba
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

Az összes felsorolása.

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

### -FabricName
Anyagnév.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProviderName
Helyreállítási szolgáltatás szolgáltatójának neve

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
A helyreállítási szolgáltatások tárolója neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az előfizetés azonosítója.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider

## MEGJEGYZÉSEK

ALIASOK

## KAPCSOLÓDÓ HIVATKOZÁSOK

