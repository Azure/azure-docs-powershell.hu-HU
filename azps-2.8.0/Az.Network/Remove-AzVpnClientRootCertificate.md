---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: ed5a2d3d004dfe1480d14e598b009cf6e49d2c1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837061"
---
# Remove-AzVpnClientRootCertificate

## Áttekintés
Eltávolítja a meglévő VPN-ügyfél legfelső szintű tanúsítványát.

## SZINTAXISA

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzVpnClientRootCertificate** parancsmag eltávolítja a megadott főtanúsítványt egy virtuális hálózati átjáróról.
A legfelső szintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót használják: az átjárón használt összes többi tanúsítvány meghatalmazza a főtanúsítványt.
Ha eltávolít egy olyan főtanúsítványos számítógépeket, amelyek a tanúsítványt a hitelesítés céljából használják, a továbbiakban nem fog tudni csatlakozni az átjáróhoz.
A **Remove-AzVpnClientRootCertificate** használata esetén mind a tanúsítvány nevét, mind a tanúsítvány adatainak szöveges ábrázolását meg kell adnia.
A tanúsítványok szöveges ábrázolásáról további információt a *PublicCertData* paraméter leírása című témakörben találhat.

## Példák

### 1. példa: az ügyfél legfelső szintű tanúsítványának eltávolítása virtuális hálózati átjáróról
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

Ez a példa eltávolítja a ContosoRootCertificate nevű ügyfél-főtanúsítványt a virtuális hálózati átjáró ContosoVirtualGateway.
Az első parancs a **Get-Content** parancsmagot használva kapja meg a tanúsítvány korábban kivitt szöveges ábrázolását; ezt a szöveges ábrázolást a $Text nevű változóban tárolja.
A második parancs ezután az a – Loop függvénnyel kinyeri az összes szöveget $Text az első és az utolsó sorának kivételével.
Ez a kibontott szöveg egy $CertificateText nevű változóban tárolódik.
A harmadik parancs a $CertificateText-változóban tárolt információkat a **Remove-AzVpnClientRootCertificate** parancsmaggal együtt a tanúsítványnak az átjáróról való eltávolítására használja.

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

### -PublicCertData
Az eltávolítani kívánt főtanúsítvány szöveges ábrázolását adja meg.
A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64-kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.
A következőhöz hasonló kimenetet kell látnia (ne feledje, hogy a tényleges kimenet több sornyi szöveget fog tartalmazni, mint az itt látható):-----megkezdi a tanúsítvány-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----záró TANÚSÍTVÁNYát-----a PublicCertData az első sor (-----KEZDÉSi tanúsítvány-----) és a fájl utolsó sora (-----záró tanúsítvány-----) között található.
A PublicCertData a következőhöz hasonló Windows PowerShell-parancsokkal lehet letölteni: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

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

### -ResourceGroupName
Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.
Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.

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

### -VirtualNetworkGatewayName
Annak a virtuális hálózati átjárónak a neve, amelyből a tanúsítványt törölték.

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

### -VpnClientRootCertificateName
Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

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

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Új – AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


