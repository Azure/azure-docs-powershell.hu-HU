---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 784374b620af09b00f460ff5c50d0a08baa46233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014019"
---
# Remove-AzNetworkInterfaceIpConfig

## Áttekintés
Hálózati kapcsolat IP-konfigurációjának eltávolítása hálózati kapcsolatból.

## SZINTAXISA

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Remove-AzNetworkInterfaceIpConfig** parancsmag egy hálózati kapcsolat IP-konfigurációját az Azure hálózati felületről távolítja el.

## Példák

### 1: IP-konfiguráció törlése hálózati felületen
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

Az első parancs a mynic nevű hálózati felületet kapja, és a változó $nic tárolja. A második parancs eltávolítja az e hálózati csatolóval társított IPConfig-1 nevű IP-konfigurációt.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Annak a hálózati kapcsolatnak az IP-konfigurációjának a nevét adja meg, amelyet el szeretne távolítani.

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

### -NetworkInterface
Egy **NetworkInterface** -objektumot ad meg.
Ez az objektum az eltávolítandó hálózati kapcsolat IP-konfigurációját tartalmazza.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
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

### Microsoft. Azure. commands. Network. models. PSNetworkInterface

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkInterface

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[Új – AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Set-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)


