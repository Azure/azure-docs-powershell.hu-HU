---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208846"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
Eltávolít egy SSL-kötést egy feltöltött tanúsítványból.

## SZINTAXIS

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzWebAppSSLBinding** parancsmag eltávolítja az SSL-kötéseket az Azure Web Appból.
Az SSL-kötések a webalkalmazások tanúsítványhoz való társítását használják.

## PÉLDÁK

### 1. példa: SSL-kötés eltávolítása webalkalmazáshoz
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Ez a parancs eltávolítja a ContosoWebApp webapp SSL-kötését.
Mivel a *DeleteCertificate* paraméter nem szerepel a paraméterben, a tanúsítvány törlődik, ha már nincs SSL-kötése.

### 2. példa: SSL-kötés eltávolítása a tanúsítvány eltávolítása nélkül
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Az 1. példához hasonlóan ez a parancs a ContosoWebApp webapp SSL-kötését is eltávolítja.
Ebben az esetben azonban szerepel a *DeleteCertificate* paraméter, és a paraméter értéke $False.
Ez azt jelenti, hogy a tanúsítvány nem törlődik, függetlenül attól, hogy rendelkezik-e SSL-kötéssel.

### 3. példa: Ssl-kötés eltávolítása objektumhivatkozással
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

Ebben a példában egy objektumhivatkozást használtunk a Web App webhelyére a webalkalmazás SSL-kötésének eltávolításához.
Az első parancs a Get-AzWebApp parancsmag használatával hoz létre egy, a ContosoWebApp nevű webalkalmazásra való hivatkozást.
Ezt az objektumhivatkozást egy $WebApp.
A második parancs az SSL-kötés eltávolításához az objektumhivatkozást és a **Remove-AzWebAppSSLBinding** parancsmagot használja.

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

### -DeleteCertificate
Azt a műveletet adja meg, amelyet akkor kell alkalmazni, ha az eltávolított SSL-kötés az egyetlen kötés, amelyet a tanúsítvány használ.
Ha *a DeleteCertificate* $False, a tanúsítvány nem törlődik a kötés törlésekor.
Ha *a DeleteCertificate* $True vagy nem szerepel a parancsban, a tanúsítvány az SSL-kötéssel együtt törlődik.
A tanúsítvány csak akkor törlődik, ha az eltávolított SSL-kötés az egyetlen kötés, amelyet a tanúsítvány használ.
Ha a tanúsítványnak több kötése van, a rendszer nem távolítja el a tanúsítványt a *DeleteCertificate* paraméter értékétől függetlenül.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A webalkalmazás nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a neve, amelyhez a tanúsítvány hozzá van rendelve.
Ugyanabban a parancsban nem használhatja az *ResourceGroupName* és a *WebApp* paramétert.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
A Web App telepítési helyének megadása.
Telepítési hely letelepítéséhez használja a Get-AzWebAppSlot parancsmagot.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Egy webalkalmazást ad meg.
Webalkalmazást a Get-AzWebApp használhat.
A *WebApp paraméter* nem használható ugyanabban a parancsban, mint az *ResourceGroupName* és/vagy a *WebAppName paraméter.*

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
A webalkalmazás nevét adja meg.
Ugyanabban a parancsban nem használhatja a *WebAppName* és a *WebApp* paramétert.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## KIMENETEK

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppszaj](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


