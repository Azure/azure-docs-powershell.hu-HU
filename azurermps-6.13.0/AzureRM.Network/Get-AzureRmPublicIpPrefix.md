---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672472"
---
# Get-AzureRmPublicIpPrefix

## Áttekintés
Nyilvános IP-előtagot kap

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Alapértelmezett
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmPublicIpPrefix** parancsmag egy vagy több nyilvános IP-előtagokat kap egy erőforráscsoport esetében.

## Példák

### Példa 1
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

Ez a parancs egy nyilvános IP-előtagot tartalmazó erőforrást kap, az erőforráscsoport $prefixName az erőforrás csoportban $rgName

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Az erőforrás neve.

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrás csoport neve.

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás-azonosító.

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction
További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String


## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSPublicIpPrefix


## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
