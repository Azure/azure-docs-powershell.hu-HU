---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367105"
---
# New-AzWebAppSSLBinding

## SYNOPSIS
Ssl-tanúsítványkötést hoz létre egy Azure Web Apphoz.

## SZINTAXIS

### S1
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzWebAppSSLBinding** parancsmag ssl-tanúsítványkötést hoz létre az Azure Web Apphoz.
A parancsmag kétféleképpen hoz létre SSL-kötést: 
- A webalkalmazásokat meglévő tanúsítványhoz kötheti.
- Feltölthet egy új tanúsítványt, majd ehhez az új tanúsítványhoz kötheti a webalkalmazást.
Függetlenül attól, hogy melyik módszert használja, a tanúsítványnak és a webalkalmazásnak ugyanannak az Azure-erőforráscsoportnak kell társítva lennie.
Ha van egy webalkalmazása az "A" erőforráscsoportban, és a webalkalmazást egy B erőforráscsoportbeli tanúsítványhoz szeretné kötni, ezt az egyetlen módszer, ha feltölti a tanúsítvány egy példányát az "A" erőforráscsoportba. Ha új tanúsítványt tölt fel, tartsa szem előtt az Azure SSL-tanúsítványra vonatkozó alábbi követelményeket: 
- A tanúsítványnak tartalmaznia kell egy titkos kulcsot. 
- A tanúsítványnak a Személyes adatcsere (PFX) formátumot kell használnia. 
- A tanúsítvány tulajdonosának meg kell egyeznie a webalkalmazás eléréséhez használt tartománnyal. 
- A tanúsítványnak legalább 2048 bites titkosítást kell használnia.

## PÉLDÁK

### 1. példa: Tanúsítvány webalkalmazáshoz kötése
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Ez a parancs egy meglévő Azure-tanúsítványt (az E3A38EBA60CAA1C1C162785A2E1C44A15AD450199C3) és a ContosoWebApp nevű webappot köti össze.

### 2. példa

Ssl-tanúsítványkötést hoz létre egy Azure Web Apphoz. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## PARAMETERS

### -CertificateFilePath
A feltöltendni kívánt tanúsítvány fájl elérési útját adja meg.
A *CertificateFilePath* paraméterre csak akkor van szükség, ha a tanúsítvány még nincs feltöltve az Azure-ba.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
A tanúsítvány visszafejtési jelszavát adja meg.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
A Web App telepítőhelyének nevét adja meg.
A Get-AzWebAppSlot használhatja.
A telepítési rések lehetőséget nyújtanak a webalkalmazások interneten keresztüli elérhetővé tétele nélkül is a webalkalmazások szakaszba helyezésére és érvényesítésére.
A módosításokat általában egy átmeneti webhelyen kell üzembe helyeznie, ellenőriznie kell a módosításokat, majd telepítenie kell az éles (internetről elérhető) webhelyre.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
Azt adja meg, hogy engedélyezve van-e a tanúsítvány.
Állítsa az *SSLState paramétert* 1-re a tanúsítvány engedélyezéséhez, vagy állítsa az *SSLState* paramétert 0-ra a tanúsítvány letiltásához.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
A tanúsítvány egyedi azonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Egy webalkalmazást ad meg.
Webalkalmazás lekérte a Get-AzWebApp parancsmagot.
A *WebApp paraméter* nem használható ugyanabban a parancsban, mint az *ResourceGroupName* és/vagy a *WebAppName paraméter.*

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Annak a webalkalmazásnak a nevét adja meg, amelyhez az új SSL-kötést létre szeretné hozatni.
Ugyanabban a parancsban nem használhatja a *WebAppName* és a *WebApp* paramétert.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## KIMENETEK

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppszaj](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


