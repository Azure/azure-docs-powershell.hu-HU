---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 389a34a5b1c34618339bb7a1752031eaafb9efe9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843610"
---
# Set-AzNetworkInterface

## Áttekintés
Egy hálózati kapcsolat cél állapotának beállítása.

## SZINTAXISA

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzNetworkInterface** az Azure-hálózati kapcsolat céljának állapotát állítja be.

## Példák

### 1. példa: hálózati felület beállítása
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

Ez a példa hálózati felületet konfigurál.
Az első parancs a NetworkInterface1 nevű hálózati felületet kapja az erőforráscsoport ResourceGroup1.
A második parancs az IP-konfiguráció privát IP-címét állítja be.
A harmadik parancs a privát IP-kiosztási módszert a statikus értékre állítja.
A negyedik parancs a hálózati felületen címkét állít be.
Az ötödik parancs a $Nic változóban tárolt információkat használja a hálózati felület beállításához.

### 2. példa: a DNS-beállítások módosítása hálózati felületen
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Az első parancs a NetworkInterface1 nevű hálózati felületet kapja, amely az erőforráscsoport ResourceGroup1 található. A második parancs hozzáadja a DNS Server 192.168.1.100 az interfészhez. A harmadik parancs ezeket a módosításokat alkalmazza a hálózati felületen. Ha el szeretne távolítani egy DNS-kiszolgálót, kövesse a fenti, de a csere "parancsot. Adja hozzá a "with" szót. "A második parancs" eltávolítása.

### 3. példa: az IP-forwading engedélyezése hálózati felületen
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja. A második parancs az IP-továbbítás értékét True értékre módosítja. Végül a harmadik parancs alkalmazza a módosításokat a hálózati felületen. Ha le szeretné tiltani az IP-továbbítást egy hálózati kapcsolaton, kövesse a minta példáját, de mindenképpen módosítsa a második parancsot "$nic. EnableIPForwarding = 0 ".

### 4. példa: egy hálózati kapcsolat alhálózatának módosítása
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Az első parancs megkapja a hálózati felületet, és a $nic változóban tárolja a NetworkInterface1. A második parancs az alhálózathoz társított virtuális hálózatot kapja meg, amelyhez a hálózati csatoló van társítva. A második parancs az alhálózatot kapja, és a $subnet 2 változóban tárolja. A harmadik parancs az új alhálózat hálózati felületének elsődleges magánhálózati IP-címével társítva. Végül az utolsó parancs alkalmazza ezeket a módosításokat a hálózati felületen.

>[!NOTE] 
>Az IP-konfigurációnak dinamikusan kell lennie ahhoz, hogy módosítani tudja az alhálózatot. Ha statikus IP-konfigurációval rendelkezik, a folytatás előtt módosítsa majd a dinamikus értékre. 

>[!NOTE]
>Ha a hálózati felület több IP-konfigurációval rendelkezik, a tovább parancsot minden IP-konfigurációnál el kell végeznie, mielőtt végrehajtja a végleges Set-AzNetworkInterface parancsot. Ezt úgy teheti meg, mint a Forth parancsban, de a "0" helyett a megfelelő számra cseréli. Ha egy hálózati kapcsolat N IP-konfigurációval rendelkezik, a fenti parancsok N-1-nek léteznie kell.

### Példa 5: hálózat biztonsági csoportjának társítása és szétválasztása hálózati kapcsolattal
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Az első parancs a NetworkInterface1 nevű meglévő hálózati felületet kapja, és a $nic változóban tárolja. A második parancs a MyNSG nevű meglévő hálózati biztonsági csoportot kapja meg, és a $nsg változóban tárolja. A Forth parancs a $nsgt a $nichez rendeli. Végül az ötödik parancs alkalmazza a módosításokat a hálózati felületen. Ha hálózati felületen szeretné szétválasztani a hálózat biztonsági csoportjait, egyszerűen cserélje $nsg a Forth parancsra $null segítségével.

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

### -NetworkInterface
Itt adhatja meg azt a **NetworkInterface** -objektumot, amely egy hálózati kapcsolat céljának állapotát jelképezi.

```yaml
Type: PSNetworkInterface
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

### PSNetworkInterface
A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkInterface

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Új – AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
