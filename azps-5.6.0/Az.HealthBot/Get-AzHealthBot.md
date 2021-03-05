---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013237"
---
# Get-AzHealthBot

## SYNOPSIS
Szerezze be a HealthBotot.

## SZINTAXIS

### Lista1 (alapértelmezett)
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Bej.le
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Lista
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## LEÍRÁS
Szerezze be a HealthBotot.

## PÉLDÁK

### 1. példa: Az összes HealthBot lekérte
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

Az összes HealthBot lekérte

### 2. példa: Az összes HealthBot lekérte a ResourceGroupName szerint
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

Az összes HealthBot lekérte: ResourceGroupName

### 3. példa: A HealthBot lekérte resourcegroupname és name szerint
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

Get HealthBot by ResourceGroupName and Name

### 4. példa: A HealthBot lekérte az InputObject eszközét
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

A HealthBot lekérte az InputObject eszközét

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
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A roboterőforrás neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A roboterőforrás-csoport neve a felhasználói előfizetésben.

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
Azure-előfizetés azonosítója.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: <IHealthBotIdentity> Identity Parameter
  - `[BotName <String>]`: A roboterőforrás neve.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[ResourceGroupName <String>]`: A roboterőforrás-csoport neve a felhasználói előfizetésben.
  - `[SubscriptionId <String>]`: Azure-előfizetés azonosítója.

## KAPCSOLÓDÓ HIVATKOZÁSOK

