---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502656"
---
# New-AzureRmApplicationGatewaySku

## Áttekintés
Egy alkalmazás-átjáró SKU-ának létrehozása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmApplicationGatewaySku** parancsmag létrehoz egy árfolyamdiagram-egységet (SKU) az Azure Application Gateway számára.

## Példák

### 1. példa: SKU létrehozása Azure Application Gateway-hez
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

Ezzel a paranccsal létrehoz egy Standard_Small nevű SKU-t egy Azure Application Gateway-nek, és az eredményt a $SKU nevű változóban tárolja.

## PARAMÉTEREK

### -Kapacitás
Az alkalmazás-átjáró példányainak számát adja meg.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A SKU nevét adja meg.

A paraméter elfogadható értékei a következők:

- Standard_Small
- Standard_Medium
- Standard_Large
- WAF_Medium
- WAF_Large

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tier (Tier)
Az SKU-típust adja meg.
A paraméter elfogadható értékei a következők:

- Standard
- WAF

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSApplicationGatewaySku

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmApplicationGatewaySku](./Get-AzureRmApplicationGatewaySku.md)

[Set-AzureRmApplicationGatewaySku](./Set-AzureRmApplicationGatewaySku.md)


