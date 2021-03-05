---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: 87b53048ede0a5b2484da18ccd0a2f6a531aa92b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008566"
---
# Get-AzSecurityAdaptiveNetworkHardening

## SYNOPSIS
Az Adaptive Network Hardenings erőforrások listája egy kiterjesztett erőforrás hatókörében.

## SZINTAXIS

### ResourceGroupLevelResource
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## LEÍRÁS
Az Adaptive Network Hardenings értékeket az Azure Biztonsági központ automatikusan kiszámítja. Ezzel a parancsmaggal lekérte az Adaptive Network Hardenings erőforrások listáját egy kiterjesztett erőforrásra terjedve.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

Az Adaptive Network Hardenings erőforrások listája egy kiterjesztett erőforrás hatókörében.

### 2. példa
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
Egyetlen Adaptive Network Hardenings erőforrás

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Erőforrás neve.

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceNamespace
Az erőforrás névtere.

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Az erőforrás típusa.

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdaptiveNetworkHardeningResourceName
Az Adaptive Network Hardening erőforrás neve.

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure-előfizetés azonosítója.

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK