---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378950"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
Ezzel a paranccsal a felhasználók létrehozhatják a Vpn ipsec házirendobjektumot, amely megadja az ipsecencryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,Group,PfsGroup értéket a VPN-átjárón. Ezzel a paranccsal a kimeneti objektum vpn ipsec-házirendet állíthat be az új/ meglévő átjárókhoz is.

## SZINTAXIS

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Ezzel a paranccsal a felhasználók létrehozhatják a Vpn ipsec házirendobjektumot, amely megadja az ipsecencryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,Group,PfsGroup értéket a VPN-átjárón. Ezzel a paranccsal a kimeneti objektum vpn ipsec-házirendet állíthat be az új/ meglévő átjárókhoz is.

## PÉLDÁK

### 1. példa: Vpn ipsec-házirendobjektum definiálása:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Ezzel a parancsmaggal hozhatja létre a vpn ipsec házirendobjektumot a felhasználó által a paraméter:VpnClientIpsecPolicy of PS parancs által át lehet adni: New-AzVirtualNetworkGateway (Új VPN-átjáró létrehozása) / Set-AzVirtualNetworkGateway (meglévő VPN-átjáró frissítése) az ResourceGroupban:

### 2. példa: Új virtuális hálózati átjáró létrehozása egyéni IPsec-házirend beállításával:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Ez a parancsmag a létrehozás után virtuális hálózati átjáróobjektumot ad vissza. 

### 3. példa: Egyéni vpn ipsec-házirend beállítása meglévő virtuális hálózati átjárón:
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Ez a parancsmag virtuális hálózati átjáróobjektumot ad vissza a vpn egyéni ipsec-házirend beállítása után.

### 4. példa: Virtuális hálózati átjárót beállítva láthatja, hogy helyesen van-e beállítva a vpn egyéni házirend:
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Ez a parancsmag virtuális hálózati átjáróobjektumot ad vissza.

## PARAMETERS

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

### -Group
Az IKE 1. fázisában használt VpnClient VPN-csoportok a kezdeti SA-hez

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
A VpnClient IKE titkosítási algoritmus (IKE 2. fázis)

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
A VpnClient IKE integritási algoritmusa (IKE 2. fázis)

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
A VpnClient IPSec titkosítási algoritmus (IKE 1. fázis)

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
A VpnClient IPSec integritási algoritmus (IKE 1. fázis)

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
Az IKE 2. fázisában használt VpnClient PFS-csoportok új gyermek biztonsági társítása esetén

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
A VpnClient IPSec biztonsági társítás (más néven gyors mód vagy 2. fázis sa) terhelési mérete KB-ban

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
A VpnClient IPSec biztonsági társítás (más néven gyorsmód vagy 2. fázis sa) élettartama másodpercben

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
