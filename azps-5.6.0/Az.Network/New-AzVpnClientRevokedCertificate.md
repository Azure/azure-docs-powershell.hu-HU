---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924665"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Létrehoz egy új VPN-ügyfél-visszavonási tanúsítványt.

## SZINTAXIS

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzVpnClientRevokedCertificate parancsmag** létrehoz egy új virtuális magánhálózati ügyfél-visszavonási tanúsítványt virtuális hálózati átjárón való használatra.
Az ügyfél-visszavonási tanúsítványok megakadályozzák, hogy az ügyfélszámítógépek a megadott tanúsítványt használják hitelesítésre.
Ez a parancsmag egy olyan különálló tanúsítványt hoz létre, amely nincs hozzárendelve egy virtuális átjáróhoz.
Ehelyett a **New-AzVpnClientRevokedCertificate** által létrehozott tanúsítványt a New-AzVirtualNetworkGateway-parancsmaggal együtt használja, amikor új átjárót hoz létre.
Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate.
Ezt a tanúsítványobjektumot használhatja új virtuális átjáró létrehozásakor.
Például: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
További információt a New-AzVirtualNetworkGateway dokumentációjában talál.

## PÉLDÁK

### 1. példa: Új ügyfél által visszavont tanúsítvány létrehozása
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Ez a parancs létrehoz egy új ügyfél által visszavont tanúsítványt, és a tanúsítványobjektumot egy $Certificate.
Ezt a változót a **New-AzVirtualNetworkGateway** parancsmag használhatja a tanúsítvány új virtuális hálózati átjáróhoz való hozzáadásához.

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

### -Name
Az új ügyfél-visszavonási tanúsítvány egyedi nevét adja meg.

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

### -Thumbprint
A hozzáadott tanúsítvány egyedi azonosítója.
A tanúsítványokhoz az ehhez hasonló Windows PowerShell-paranccsal is vissza lehet nyomtatni a tanúsítványokat: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Az előző parancs a gyökértanúsítvány-tárolóban található összes helyi számítógéptanúsítvány adatait adja vissza.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


