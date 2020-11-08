---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184287"
---
# Get-AzPolicyMetadata

## Áttekintés
Házirend metaadat-erőforrásainak beolvasása

## SZINTAXISA

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzPolicyRemediation** parancsmag minden házirend metaadat-erőforrását vagy egy bizonyos házirend metaadat-erőforrást kap.

## Példák

### Példa 1: a házirend metaadat-erőforrásainak beolvasása
```powershell
PS C:\> Get-AzPolicyMetadata
```

Ez a parancs minden házirend metaadat-erőforrását kinyeri

### 2. példa: 10 házirend metaadat-erőforrásának beszerzése
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Ez a parancs 10 házirend metaadat-erőforrásának gyűjteményét kapja

### 3. példa: egyetlen házirend metaadat-erőforrásának beszerzése a ' ACF1348 ' névvel
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Ez a parancs egyetlen házirend-metaadat-erőforrást kap a "ACF1348" névvel.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
Erőforrás neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Az eredményül adott házirend metaadat-erőforrásainak maximális száma.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. PolicyInsights. models. PSPolicyMetadata

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
