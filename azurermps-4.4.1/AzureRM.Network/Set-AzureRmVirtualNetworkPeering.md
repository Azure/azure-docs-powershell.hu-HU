---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493408"
---
# Set-AzureRmVirtualNetworkPeering

## Áttekintés
Virtuális hálózat egyszemélyes nézetének beállítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmVirtualNetworkPeering** parancsmag virtuális hálózat-összehívást konfigurál.

## Példák

### 1. példa: a virtuális hálózati kapcsolat továbbított forgalmi konfigurációjának módosítása
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### 2. példa: virtuális hálózati kapcsolat virtuális hálózati hozzáférésének módosítása
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### 3. példa: a virtuális hálózat társközi átviteli tulajdonságának módosítása
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### Példa 4: távoli átjárók használata a virtuális hálózatban
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

Ha ezt a tulajdonságot $Truere módosítja, akkor a VNet átjárója használható.
A társközi VNet azonban konfigurálnia kell az átjárót, és a **AllowGatewayTransit** értéke $true kell, hogy legyen.

Ez a tulajdonság nem használható, ha egy átjáró már konfigurálva van.

## PARAMÉTEREK

### -VirtualNetworkPeering
A virtuális hálózat társközi beállítását adja meg.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### PSVirtualNetworkPeering
A ' VirtualNetworkPeering ' paraméter az "PSVirtualNetworkPeering" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmVirtualNetworkPeering](./Add-AzureRmVirtualNetworkPeering.md)

[Get-AzureRmVirtualNetworkPeering](./Get-AzureRmVirtualNetworkPeering.md)

[Remove-AzureRmVirtualNetworkPeering](./Remove-AzureRmVirtualNetworkPeering.md)


