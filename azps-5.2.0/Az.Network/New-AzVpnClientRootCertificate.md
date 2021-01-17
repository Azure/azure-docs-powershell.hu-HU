---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336581"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
Létrehoz egy új VPN-ügyfél legfelső szintű tanúsítványt.

## SZINTAXIS

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzVpnClientRootCertificate** parancsmag létrehoz egy új VPN-gyökértanúsítványt virtuális hálózati átjárón való használatra.
A főtanúsítványok olyan X.509-tanúsítványok, amelyek azonosítják a legfelső szintű hitelesítésszolgáltatót: az átjárón használt összes többi tanúsítvány megbízik a legfelső szintű tanúsítványban.
Ez a parancsmag egy olyan különálló tanúsítványt hoz létre, amely nincs hozzárendelve egy virtuális átjáróhoz.
Ehelyett a **New-AzVpnClientRootCertificate** által létrehozott tanúsítványt a New-AzVirtualNetworkGateway parancsmaggal együtt használja új átjáró létrehozásakor.
Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate.
Ezt a tanúsítványobjektumot használhatja új virtuális átjáró létrehozásakor.
Például: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
További információt a New-AzVirtualNetworkGateway dokumentációjában talál.

## PÉLDÁK

### 1. példa: Ügyfél-főtanúsítvány létrehozása
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

Ebben a példában egy ügyfél-gyökértanúsítványt hoz létre, és a tanúsítványobjektumot egy "$Certificate" nevű változóban $Certificate.
Ezt a változót a **New-AzVirtualNetworkGateway** parancsmag arra használhatja, hogy gyökértanúsítványt adjon hozzá egy új virtuális hálózati átjáróhoz.
Az első parancs a **Get-Content** parancsmagot használja a gyökértanúsítvány korábban exportált szövegként való megjelenítéséhez; hogy a szöveges adatokat egy $Text.
A második parancs ezután egy hurok segítségével kinyeri az összes szöveget, kivéve az első és az utolsó sort, és a kinyert szöveget egy új nevű változóban $CertificateText.
A harmadik parancs a **New-AzVpnClientRootCertificate** parancsmagot használja a tanúsítvány létrehozásához, és a létrehozott objektumot egy $Certificate.

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
Az új ügyfél legfelső szintű tanúsítványának nevét adja meg.

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
Megadja a hozzáadni szükséges főtanúsítvány szövegként való megjelenítését.
A szöveg reprezentáció beszerzéséhez exportálja a tanúsítványt .cer formátumban (Base64 kódolással), majd nyissa meg az így kapott fájlt egy szövegszerkesztőben.
Ehhez hasonló kimenetet kell látnia (ne feledje, hogy a tényleges kimenet az itt látható rövidített mintaszövegnél sokkal több szövegsort fog tartalmazni): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.
A PublicCertData lekérdezéséhez a következő Windows PowerShell-parancsokat használhatja: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


