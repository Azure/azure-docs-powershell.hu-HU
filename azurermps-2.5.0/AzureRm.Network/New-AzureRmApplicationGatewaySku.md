---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: cda4281b1bf52b9f0b94926bc66590d1bd741c44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848769"
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
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Name (név)
A SKU nevét adja meg.

A paraméter elfogadható értékei a következők:

- Standard_Small
- Standard_Medium
- Standard_Large
- WAF_Medium
- WAF_Large

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
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


