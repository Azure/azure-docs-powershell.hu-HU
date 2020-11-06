---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: 8403a2e26bbc149db35c9c20cdea3075adb88492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494807"
---
# Set-AzureRmNetworkInterface

## Áttekintés
Egy hálózati kapcsolat cél állapotának beállítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmNetworkInterface** az Azure-hálózati kapcsolat céljának állapotát állítja be.

## Példák

### 1. példa: hálózati felület beállítása
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

Ez a példa hálózati felületet konfigurál.
Az első parancs a NetworkInterface1 nevű hálózati felületet kapja az erőforráscsoport ResourceGroup1.
A második parancs az IP-konfiguráció privát IP-címét állítja be.
A harmadik parancs a privát IP-kiosztási módszert a statikus értékre állítja.
A negyedik parancs a hálózati felületen címkét állít be.
Az ötödik parancs a $Nic változóban tárolt információkat használja a hálózati felület beállításához.

### 2. példa: a DNS-beállítások módosítása hálózati felületen
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

Az első parancs a NetworkInterface1 nevű hálózati felületet kapja, amely az erőforráscsoport ResourceGroup1 található. A második parancs hozzáadja a DNS Server 192.168.1.100 az interfészhez. A harmadik parancs ezeket a módosításokat alkalmazza a hálózati felületen. Ha el szeretne távolítani egy DNS-kiszolgálót, kövesse a fenti, de a csere "parancsot. Adja hozzá a "with" szót. "A második parancs" eltávolítása.

### 3. példa: az IP-forwading engedélyezése hálózati felületen
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja. A második parancs az IP-továbbítás értékét True értékre módosítja. Végül a harmadik parancs alkalmazza a módosításokat a hálózati felületen. Ha le szeretné tiltani az IP-továbbítást egy hálózati kapcsolaton, kövesse a minta példáját, de mindenképpen módosítsa a második parancsot "$nic. EnableIPForwarding = 0 ".

### 4. példa: egy hálózati kapcsolat alhálózatának módosítása
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

Az első parancs megkapja a hálózati felületet, és a $nic változóban tárolja a NetworkInterface1. A második parancs az alhálózathoz társított virtuális hálózatot kapja meg, amelyhez a hálózati csatoló van társítva. A második parancs az alhálózatot kapja, és a $subnet 2 változóban tárolja. A harmadik parancs az új alhálózat hálózati felületének elsődleges magánhálózati IP-címével társítva. Végül az utolsó parancs alkalmazza ezeket a módosításokat a hálózati felületen.

>[!NOTE] 
>Az IP-konfigurációnak dinamikusan kell lennie ahhoz, hogy módosítani tudja az alhálózatot. Ha statikus IP-konfigurációval rendelkezik, a folytatás előtt módosítsa majd a dinamikus értékre. 

>[!NOTE]
>Ha a hálózati felület több IP-konfigurációval rendelkezik, a tovább parancsot minden IP-konfigurációnál el kell végeznie, mielőtt végrehajtja a végleges Set-AzureRmNetworkInterface parancsot. Ezt úgy teheti meg, mint a Forth parancsban, de a "0" helyett a megfelelő számra cseréli. Ha egy hálózati kapcsolat N IP-konfigurációval rendelkezik, a fenti parancsok N-1-nek léteznie kell.

### Példa 5: hálózat biztonsági csoportjának társítása és szétválasztása hálózati kapcsolattal
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja. A második parancs a MyNSG nevű meglévő hálózati biztonsági csoportot kapja meg, és a $nsg változóban tárolja. A Forth parancs a $nsgt a $nichez rendeli. Végül az ötödik parancs alkalmazza a módosításokat a hálózati felületen. Ha hálózati felületen szeretné szétválasztani a hálózat biztonsági csoportjait, egyszerűen cserélje $nsg a Forth parancsra $null segítségével.

## PARAMÉTEREK

### -NetworkInterface
Itt adhatja meg azt a **NetworkInterface** -objektumot, amely egy hálózati kapcsolat céljának állapotát jelképezi.

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

### PSNetworkInterface
A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkInterface

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[Új – AzureRmNetworkInterface](./New-AzureRmNetworkInterface.md)

[Remove-AzureRmNetworkInterface](./Remove-AzureRmNetworkInterface.md)
