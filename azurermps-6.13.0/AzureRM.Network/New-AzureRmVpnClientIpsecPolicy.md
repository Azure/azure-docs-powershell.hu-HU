---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504328"
---
# New-AzureRmVpnClientIpsecPolicy

## Áttekintés
Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van Ez a parancs lehetővé teszik a kimenő objektum a VPN-alapú IPSec-házirend beállítását az új/exisitng átjárók számára.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van Ez a parancs lehetővé teszik a kimenő objektum a VPN-alapú IPSec-házirend beállítását az új/exisitng átjárók számára.

## Példák

### Virtuális magánhálózati IPSec-házirend-objektum meghatározása:
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Ezzel a parancsmaggal létrehozhatja a virtuális magánhálózati IPSec-házirend objektumát az átadott egy vagy minden paraméter értékével, amelyet a felhasználó átadhat a param: VpnClientIpsecPolicy a PS parancs segítségével: New-AzureRmVirtualNetworkGateway (új VPN-átjáró létrehozása)/Set-AzureRmVirtualNetworkGateway (meglévő VPN-átjáró frissítése) a ResourceGroup:

### Új virtuális hálózati átjáró létrehozása a VPN-alapú egyéni IPSec-házirend beállításával:
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Ez a parancsmag a létrehozás után a virtuális hálózati átjáró objektum értékét jeleníti meg. 

### Egyéni virtuális magánhálózati IPSec-házirend beállítása a meglévő virtuális hálózati átjárón:
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Ez a parancsmag a virtuális hálózati átjáró objektumot a virtuális magánhálózati IPSec-házirend beállítása után ad eredményül.

### Virtuális hálózati átjáró beszerzése annak megállapításához, hogy helyesen van-e beállítva a VPN-házirend:
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Ez a parancsmag a virtuális hálózati átjáró objektum értékét jeleníti meg.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DhGroup
Az IKE-fázis 1-es verziójában az első biztonsági társításhoz használt vpnclient DH-csoportok

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
A vpnclient IKE titkosítási algoritmusa (IKE Phase 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
A vpnclient IKE Integrity algoritmusa (IKE Phase 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
Az vpnclient IPSec titkosítási algoritmusa (IKE Phase 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecIntegrity
A vpnclient IPSec Integrity algoritmusa (IKE Phase 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
A vpnclient PFS-csoportok az IKE Phase 2 for New Child SA alkalmazásban

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
A vpnclient IPSec biztonsági társítása (más néven gyorsmódú vagy Phase 2 SA) terhelési mérete KB-ban

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
A vpnclient IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) élettartama másodpercben

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSIpsecPolicy

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
