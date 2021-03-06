---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: f83a0f34e23822d5d6ff7c55236fdb81065b7f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005909"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
Eltávolít egy meglévő VPN-ügyféltanúsítványt.

## SZINTAXIS

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzVpnClientRootCertificate** parancsmag eltávolítja a megadott főtanúsítványt egy virtuális hálózati átjáróból.
A főtanúsítványok olyan X.509-tanúsítványok, amelyek azonosítják a legfelső szintű hitelesítésszolgáltatót: az átjárón használt összes többi tanúsítvány megbízik a legfelső szintű tanúsítványban.
Ha eltávolít egy olyan főtanúsítvány-számítógépet, amely hitelesítési célokra használja a tanúsítványt, a továbbiakban nem tud csatlakozni az átjáróhoz.
A **Remove-AzVpnClientRootCertificate** használatakor meg kell adnunk a tanúsítvány nevét és a tanúsítványadatok szövegként való megjelenítését is.
A tanúsítványok szövegként való megjelenítéséről a *PublicCertData* paraméter leírásában található további információ.

## PÉLDÁK

### 1. példa: Ügyfél legfelső szintű tanúsítványának eltávolítása virtuális hálózati átjáróból
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

Ez a példa eltávolítja a ContosoRootCertificate nevű ügyfélgyanúsítványt a ContosoVirtualGateway virtuális hálózati átjáróból.
Az első parancs a **Get-Content** parancsmagot használja a tanúsítvány korábban exportált szövegként való megjelenítéséhez; ezt a szövegként való ábrázolás egy $Text.
A második parancs ezután egy hurok segítségével kinyeri az összes szöveget a $Text az első és az utolsó sor kivételével.
Ez a kinyert szöveg egy $CertificateText.
A harmadik parancs a $CertificateText változóban tárolt információkat és a **Remove-AzVpnClientRootCertificate** parancsmagot használja a tanúsítvány eltávolításához az átjáróból.

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
Az eltávolítható főtanúsítvány szöveges ábrázolása.
A szöveg reprezentáció beszerzéséhez exportálja a tanúsítványt .cer formátumban (Base64 kódolással), majd nyissa meg az így kapott fájlt egy szövegszerkesztőben.
Az alábbihoz hasonló kimenetet kell látnia (ne feledje, hogy a tényleges kimenet az itt látható rövidített mintaszövegnél több szövegsort fog tartalmazni): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.
A PublicCertData-adatbázist a következő Windows PowerShell-parancsokkal tudja lekérni: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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
Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró hozzá van rendelve.
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
Annak a virtuális hálózati átjárónak a nevét adja meg, amelyből a tanúsítványt eltávolítja.

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
Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelyről a parancsmag eltávolítja.

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

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


