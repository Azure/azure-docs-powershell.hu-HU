---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843613"
---
# Set-AzNetworkSecurityGroup

## Áttekintés
Egy hálózati biztonsági csoport cél állapotának beállítása.

## SZINTAXISA

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzNetworkSecurityGroup** parancsmag az Azure hálózati biztonsági csoport cél állapotát állítja be.

## Példák

### Példa 1: egy hálózati biztonsági csoport cél állapotának beállítása
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

Ez a parancs beolvassa a Nsg1 nevű Azure hálózat biztonsági csoportját, és felvesz egy Rdp-Rule nevű hálózati biztonsági szabályt, amely lehetővé teszi a 3389-as porton lévő internetes forgalom engedélyezését a AzNetworkSecurityRuleConfig segítségével.
A parancs a **set-AzNetworkSecurityGroup** használatával megmarad a módosított Azure hálózat biztonsági csoportja.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSNetworkSecurityGroup
A ' NetworkSecurityGroup ' paraméter az "PSNetworkSecurityGroup" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNetworkSecurityGroup](./Get-AzNetworkSecurityGroup.md)

[Új – AzNetworkSecurityGroup](./New-AzNetworkSecurityGroup.md)

[Remove-AzNetworkSecurityGroup](./Remove-AzNetworkSecurityGroup.md)


