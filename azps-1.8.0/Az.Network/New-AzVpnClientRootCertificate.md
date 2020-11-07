---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 4d05680951585f0b5271c291cb893a28f822a6fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670241"
---
# New-AzVpnClientRootCertificate

## Áttekintés
Létrehoz egy új VPN-ügyfél főtanúsítványát.

## SZINTAXISA

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzVpnClientRootCertificate** parancsmag létrehoz egy új virtuális magánhálózati tanúsítványt a virtuális hálózati átjárón való használatra.
A legfelső szintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót használják: az átjárón használt összes többi tanúsítvány meghatalmazza a főtanúsítványt.
Ez a parancsmag olyan különálló tanúsítványt hoz létre, amely nem egy virtuális átjáróhoz van társítva.
Ehelyett az **új AzVpnClientRootCertificate** által létrehozott tanúsítványt az New-AzVirtualNetworkGateway parancsmaggal együtt használják új átjáró létrehozásakor.
Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate nevű változóban tárolja.
Ezt a objektumtípust akkor használhatja, ha új virtuális átjárót hoz létre.
Például `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
További információt az New-AzVirtualNetworkGateway parancsmag dokumentációjában talál.

## Példák

### 1. példa: aclient-főtanúsítvány létrehozása
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

Ez a példa létrehoz egy ügyfélalkalmazás főtanúsítványát, és a tanúsítvány-objektumot egy $Certificate nevű változóban tárolja.
Ezt a változót a **New-AzVirtualNetworkGateway** parancsmag használhatja a root tanúsítvány új virtuális hálózati átjáróhoz való hozzáadására.
Az első parancs a **Get-Content** parancsmagot használva kapja meg a legfelső szintű tanúsítvány korábban exportált szövegét. a program a szöveges adatot egy $Text nevű változóban tárolja.
A második parancs ezután az a – Loop függvénnyel Kinyeri a szöveget az első és az utolsó sor kivételével, a kibontott szöveget a $CertificateText nevű változóban tárolja.
A harmadik parancs a **New-AzVpnClientRootCertificate** parancsmagot használja a tanúsítvány létrehozásához, és a létrehozott objektumot a $Certificate nevű változóban tárolja.

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
Az új ügyfél főtanúsítványának nevét adja meg.

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

### -PublicCertData
A hozzáadni kívánt főtanúsítvány szöveges ábrázolását adja meg.
A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64 kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.
A kimenethez hasonló kimenetet kell látnia (Megjegyzendő, hogy a tényleges kimenet több sornyi szöveget fog tartalmazni, mint az itt látható):-----a tanúsítvány megkezdése-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----záró TANÚSÍTVÁNYát,-----a PublicCertData az első sor (-----KEZDÉSi tanúsítvány-----) és a fájl utolsó sora (-----záró tanúsítvány-----) közötti sorokból áll.
A PublicCertData a következőhöz hasonló Windows PowerShell-parancsokkal lehet letölteni: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. hossza-1; $i + +) {$Text \[ $i \] }

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


