---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345834"
---
# Set-AzNetworkInterface

## SYNOPSIS
Frissíti a hálózati felületet.

## SZINTAXIS

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzNetworkInterface** frissíti a hálózati felületet.

## PÉLDÁK

### 1. példa: Hálózati felület beállítása
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

Ez a példa hálózati felületet konfigurál.
Az első parancs egy NetworkInterface1 nevű hálózati felületet kap az ResourceGroup1 erőforráscsoportban.
A második parancs beállítja az IP-konfiguráció privát IP-címét.
A harmadik parancs statikusra állítja a privát IP-terhelési módot.
A negyedik parancs címkét állít be a hálózati felületen.
Az ötödik parancs a $Nic változóban tárolt információkat használja a hálózati felület beállításához.

### 2. példa: A DNS-beállítások módosítása hálózati felületen
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Az első parancs egy NetworkInterface1 nevű hálózati felületet kap, amely az ResourceGroup1 erőforráscsoportban található. A második parancs hozzáadja a 192.168.1.100-as DNS-kiszolgálót ehhez a felülethez. A harmadik parancs ezeket a módosításokat a hálózati felületre alkalmazza. DNS-kiszolgáló eltávolításához kövesse a fent felsorolt parancsokat, de cserélje le a ". Add" with ". Remove" (Eltávolítás) gombra a második parancsban.

### 3. példa: IP-továbbítás engedélyezése hálózati felületen
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Az első parancs egy NetworkInterface1 nevű meglévő hálózati felületet kap, és azt egy másik változóban $nic tárolja. A második parancs igazra módosítja az IP-továbbítás értékét. Végül a harmadik parancs alkalmazza a módosításokat a hálózati felületen. Ha hálózati felületen szeretné letiltani az IP-továbbítást, kövesse a példát, de a második parancsot mindenképpen módosítsa "$nic. EnableIPForwarding = 0".

### 4. példa: Hálózati felület alhálózatának módosítása
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Az első parancs a NetworkInterface1 hálózati felületet kapja meg, és a $nic tárolja. A második parancs annak az alhálózatnak a virtuális hálózatát kapja meg, amelyhez a hálózati felület társítva lesz. A második parancs beveszi az alhálózatot, és a $subnet 2 változóban tárolja. A harmadik parancs a hálózati felület elsődleges privát IP-címét társította az új alhálózattal. Végül az utolsó parancs alkalmazta ezeket a módosításokat a hálózati felületen.
>[!NOTE] 
>Az IP-konfigurációknak dinamikusnak kell lennie az alhálózat módosítása előtt. Ha statikus IP-konfigurációja van, a folytatás előtt váltsa át dinamikusra. 
>[!NOTE]
>Ha a hálózati felületnek több IP-konfigurációja van, az összes ilyen IP-konfiguráció esetén el kell végeznie a oda-vissza parancsot, mielőtt végrehajtja az Set-AzNetworkInterface parancsot. Ezt a "0" helyett a megfelelő számra cserélheti, mint a oda-vissza parancsban. Ha egy hálózati felület N IP-konfigurációval rendelkezik, akkor a parancsok közül N-1-nek kell léteznie.

### 5. példa: Hálózati biztonsági csoport társítása hálózati felülettel
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Az első parancs egy NetworkInterface1 nevű meglévő hálózati felületet kap, és azt egy másik változóban $nic tárolja. A második parancs egy MyNSG nevű meglévő hálózatbiztonsági csoportot kap, és azt a $nsg tárolja. A harmadik parancs hozzárendeli a $nsg a $nic. Végül a "oda" parancs alkalmazza a módosításokat a Hálózati felületen. Ha hálózati felületről származó hálózati biztonsági csoportokat $nsg a harmadik parancsban, cserélje le a $null.

## PARAMETERS

### -AsJob
Parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -NetworkInterface
Egy hálózati felületi objektumot ad meg, amely azt az állapotot jelzi, amelyben a hálózati felületet be kell állítani.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
