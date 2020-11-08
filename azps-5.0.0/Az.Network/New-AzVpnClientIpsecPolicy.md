---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195359"
---
# New-AzVpnClientIpsecPolicy

## Áttekintés
Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van Ez a parancs lehetővé teszik a kimeneti objektumnak a VPN-alapú IPSec-házirend beállítását az új/meglévő átjáróhoz.

## SZINTAXISA

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Ez a parancs lehetővé teszi a felhasználóknak, hogy hozzanak létre egy VPN-alapú IPSec-házirend-objektumot, amely egy vagy minden olyan értéket (például IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup) ad meg, amely a VPN-átjárón van Ez a parancs lehetővé teszik a kimeneti objektumnak a VPN-alapú IPSec-házirend beállítását az új/meglévő átjáróhoz.

## Példák

### 1. példa: a VPN IPSec-házirend-objektum meghatározása:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Ezzel a parancsmaggal létrehozhatja a virtuális magánhálózati IPSec-házirend objektumát az átadott egy vagy minden paraméter értékével, amelyet a felhasználó átadhat a param: VpnClientIpsecPolicy a PS parancs segítségével: New-AzVirtualNetworkGateway (új VPN-átjáró létrehozása)/Set-AzVirtualNetworkGateway (meglévő VPN-átjáró frissítése) a ResourceGroup:

### 2. példa: új virtuális hálózati átjáró létrehozása a VPN-alapú egyéni IPSec-házirend beállításával:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Ez a parancsmag a létrehozás után a virtuális hálózati átjáró objektum értékét jeleníti meg. 

### 3. példa: virtuális magánhálózati IPSec-házirend beállítása a meglévő virtuális hálózati átjáróhoz:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Ez a parancsmag a virtuális hálózati átjáró objektumot a virtuális magánhálózati IPSec-házirend beállítása után ad eredményül.

### 4. példa: a virtuális hálózat átjárójának beszerzése annak megállapításához, hogy helyesen van-e beállítva a VPN-házirend:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Ez a parancsmag a virtuális hálózati átjáró objektum értékét jeleníti meg.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DhGroup
Az IKE-fázis 1-es verziójában az első biztonsági társításhoz használt VpnClient DH-csoportok

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
A VpnClient IKE titkosítási algoritmusa (IKE Phase 2)

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
A VpnClient IKE Integrity algoritmusa (IKE Phase 2)

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
Az VpnClient IPSec titkosítási algoritmusa (IKE Phase 1)

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
A VpnClient IPSec Integrity algoritmusa (IKE Phase 1)

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
A VpnClient PFS-csoportok az IKE Phase 2 for New Child SA alkalmazásban

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
A VpnClient IPSec biztonsági társítása (más néven gyorsmódú vagy Phase 2 SA) terhelési mérete KB-ban

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
A VpnClient IPSec biztonsági társítás (más néven gyorsmódú vagy Phase 2 SA) élettartama másodpercben

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSIpsecPolicy

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
