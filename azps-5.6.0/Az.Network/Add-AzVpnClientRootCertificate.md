---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932442"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
HOZZÁAD egy VPN-ügyfél legfelső szintű tanúsítványt.

## SZINTAXIS

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzVpnClientRootCertificate** parancsmag hozzáad egy főtanúsítványt egy virtuális hálózati átjáróhoz.
A főtanúsítványok olyan X.509-es tanúsítványok, amelyek azonosítják a legfelső szintű hitelesítésszolgáltatót.
Az átjárón használt összes tanúsítvány terv szerint megbízik a főtanúsítványban.
Ez a parancsmag egy meglévő tanúsítványt rendel hozzá átjáró-főtanúsítványként.
Ha nem rendelkezik X.509-es tanúsítvánnyal, létrehozhat egyet a nyilvános kulcsú infrastruktúrán keresztül, vagy használhat egy tanúsítványkészítőt, például az makecert.exe.
Gyökértanúsítvány hozzáadásához meg kell adnia a tanúsítvány nevét, és csak szövegesen kell megadnia a tanúsítványt (további információért lásd a *PublicCertData* paramétert).
Az Azure lehetővé teszi több főtanúsítvány hozzárendelését egy átjáróhoz.
Több főtanúsítványt gyakran helyeznek üzembe olyan szervezetek, amelyek egynél több cég felhasználóit is magukban foglalják.

## PÉLDÁK

### 1. példa: Ügyfél legfelső szintű tanúsítványának hozzáadása virtuális átjáróhoz
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Ebben a példában egy ügyfél-főtanúsítványt ad hozzá a ContosoVirtualGateway nevű virtuális átjáróhoz.
Az első parancs **a Get-Content** parancsmag használatával bekéri a legfelső szintű tanúsítvány korábban exportált szövegét, és tárolja a $Text.
A második parancs ezután egy hurok segítségével kinyeri az összes szöveget, kivéve az első és az utolsó sort.
A kinyert szöveget egy $CertificateText.
A harmadik parancs ezután a $CertificateText-ben tárolt szöveget használja az **Add-AzVpnClientRootCertificate** parancsmaggal a legfelső szintű tanúsítvány hozzáadásához az átjáróhoz.

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

### -PublicCertData
A hozzáadni szükséges főtanúsítvány szövegként való ábrázolása.
A szöveg reprezentáció beszerzéséhez exportálja a tanúsítványt .cer formátumban (Base64 kódolással), majd nyissa meg az így kapott fájlt egy szövegszerkesztőben.
Ha így van, az alábbihoz hasonló kimenetet fog látni (vegye figyelembe, hogy a tényleges kimenet sokkal több szövegsort fog tartalmazni, mint az itt látható rövidített minta): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.
Ezek az adatok az ehhez hasonló Windows PowerShell-parancsokkal szerezhetők be: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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
Annak az erőforráscsoportnak a nevét adja meg, amelyhez a főtanúsítvány hozzá van rendelve.
Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.

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
Annak a virtuális hálózati átjárónak a nevét adja meg, ahol a tanúsítványt hozzáadta.

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
Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelybe a parancsmag hozzáadja.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


