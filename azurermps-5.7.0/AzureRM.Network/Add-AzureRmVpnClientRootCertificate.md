---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 11b4d3cca8d7cad8d3fb4cfcc4e256d1934592d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493118"
---
# Add-AzureRmVpnClientRootCertificate

## Áttekintés
VPN-ügyfél legfelső szintű tanúsítványát adja hozzá.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmVpnClientRootCertificate** parancsmag főtanúsítványot ad egy virtuális hálózati átjáróhoz.
A gyökérszintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót hitelesítik.
Tervezéssel minden olyan tanúsítvány, amely az átjárón a legfelső szintű tanúsítványt használja.

Ez a parancsmag egy meglévő tanúsítványt rendel el átjáró legfelső szintű tanúsítványként.
Ha nincs olyan X. 509 tanúsítvány, amellyel létrehozhatja a nyilvános kulcsú infrastruktúráját, vagy használhatja a tanúsítványt Generator (például makecert.exe) segítségével.

Főtanúsítvány hozzáadásához meg kell adnia a tanúsítvány nevét, és csak szöveges formátumban kell megadnia a tanúsítványt (további információt *a PublicCertData* paraméterben talál).
Az Azure lehetővé teszi, hogy egynél több főtanúsítványt rendeljen egy átjáróhoz.
A több főtanúsítványt gyakran olyan szervezetek telepítik, amelyek egynél több vállalat felhasználóit tartalmazzák.

## Példák

### 1. példa: az ügyfél legfelső szintű tanúsítványának felvétele virtuális átjáróba
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Ez a példa a ContosoVirtualGateway nevű virtuális átjáróhoz hozzáadja az ügyfél főtanúsítványát.

Az első parancs a **Get-Content** parancsmagot használva kapja meg a legfelső szintű tanúsítvány korábban exportált szöveges ábrázolását, és tárolja a szöveges adatok a $Text nevű változót.

A második parancs ezután az a – Loop függvénnyel kinyeri az összes szövegrészt, az első és az utolsó soron kívül.
A kibontott szöveg egy $CertificateText nevű változóban tárolódik.

A harmadik parancs ezután a $CertificateText-ban tárolt szöveget használja az **Add-AzureRmVpnClientRootCertificate** parancsmaggal a főtanúsítványnak az átjáróhoz való hozzáadásához.

## PARAMÉTEREK

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

### -PublicCertData
A beadni kívánt főtanúsítvány szöveges ábrázolását adja meg.
A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64 kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.
Ezt követően az alábbihoz hasonló kimenet jelenik meg (a tényleges kimenet több sornyi szöveget fog tartalmazni, mint a rövidített minta):

----------MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w megkezdése-----a záró tanúsítvány-----

A PublicCertData az első sor (-----KEZDÉSi-----) és az utolsó sor (-----záró tanúsítvány-----) közötti minden sorból áll.
Ezeket az adatforrásokat az alábbihoz hasonló Windows PowerShell-parancsok segítségével tudja letölteni: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnek a neve, amelyhez a főtanúsítvány van rendelve.

Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Annak a virtuális hálózati átjárónak a neve, amelybe a tanúsítványt felveszi.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRootCertificateName
Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelyre a parancsmag ad.

```yaml
Type: String
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

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[Új – AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)

[Remove-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


