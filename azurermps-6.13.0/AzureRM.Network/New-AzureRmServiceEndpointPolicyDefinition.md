---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501999"
---
# New-AzureRmServiceEndpointPolicyDefinition

## Áttekintés
{{Töltse ki a szinopszist}}

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmServiceEndpointPolicyDefinition** parancsmag a szolgáltatás végpont-házirendjének definícióját hozza létre.

## Példák

### Példa 1: szolgáltatás végpont-házirendjének létrehozása
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

Ez a parancs létrehozza a szolgáltatás végpontjának házirend-definícióját a name ServiceEndpointPolicyDefinition1, a Service Microsoft. Storage, a Service Resources-előfizetés/sub1 és a Description (új definíció) című témakörben, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $policydef változóban tárolja.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Leírás
A definíció leírása

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

### -Name (név)
A szolgáltatás végpont-házirendjének neve

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szolgáltatás
A szolgáltatás neve

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

### -ServiceResource
A szolgáltatási erőforrások listája

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction
További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs


## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicyDefinition


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
