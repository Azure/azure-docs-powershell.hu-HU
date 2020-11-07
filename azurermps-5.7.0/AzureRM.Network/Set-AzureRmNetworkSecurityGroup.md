---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: ab009608100bc4cbb4915f6bc3e82d44d9e08cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679878"
---
# Set-AzureRmNetworkSecurityGroup

## Áttekintés
Egy hálózati biztonsági csoport cél állapotának beállítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmNetworkSecurityGroup** parancsmag az Azure hálózati biztonsági csoport cél állapotát állítja be.

## Példák

### Példa 1: egy hálózati biztonsági csoport cél állapotának beállítása
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

Ez a parancs beolvassa a Nsg1 nevű Azure hálózat biztonsági csoportját, és felvesz egy Rdp-Rule nevű hálózati biztonsági szabályt, amely lehetővé teszi a 3389-as porton lévő internetes forgalom engedélyezését a AzureRmNetworkSecurityRuleConfig segítségével.
A parancs a **set-AzureRmNetworkSecurityGroup** használatával megmarad a módosított Azure hálózat biztonsági csoportja.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### -NetworkSecurityGroup
Egy hálózati biztonsági csoport objektuma, amely annak a célnak az állapotát jelenti, amelyhez a parancsmag a hálózat biztonsági csoportját állítja be.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSNetworkSecurityGroup
A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmNetworkSecurityGroup](./Get-AzureRmNetworkSecurityGroup.md)

[Új – AzureRmNetworkSecurityGroup](./New-AzureRmNetworkSecurityGroup.md)

[Remove-AzureRmNetworkSecurityGroup](./Remove-AzureRmNetworkSecurityGroup.md)


