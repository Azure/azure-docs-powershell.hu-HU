---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194961"
---
# Remove-AzWebAppSSLBinding

## Áttekintés
SSL-kötés eltávolítása feltöltött tanúsítványból.

## SZINTAXISA

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

## Leírás
A **Remove-AzWebAppSSLBinding** parancsmag egy biztonságos szoftvercsatorna-RÉTEGET (SSL-kötést) távolít el az Azure Web App alkalmazásból.
Az SSL-kötések segítségével webalkalmazásokat társíthat egy tanúsítványhoz.

## Példák

### 1. példa: egy webalkalmazás SSL-kötésének eltávolítása
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Ez a parancs eltávolítja a Web App ContosoWebApp tartozó SSL-kötést.
Mivel a *DeleteCertificate* paraméter nem szerepel a listában, a rendszer törli a tanúsítványt, ha már nincs SSL-kötése.

### 2. példa: SSL-kötés eltávolítása a tanúsítvány eltávolítása nélkül
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Az 1 értékhez hasonlóan a parancs eltávolítja az SSL-kötést a Web App ContosoWebApp.
Ebben az esetben azonban a *DeleteCertificate* paraméter szerepel, és a paraméter értéke $false értékre van állítva.
Ez azt jelenti, hogy a tanúsítvány nem törlődik, függetlenül attól, hogy SSL-kötést tartalmaz-e vagy sem.

### 3. példa: egy objektum-hivatkozás használatával eltávolíthatja az SSL-kötést
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

Ez a példa egy objektum hivatkozását használja a webalkalmazás webhelyére a webalkalmazások SSL-kötésének eltávolításához.
Az első parancs az Get-AzWebApp parancsmagot használja a ContosoWebApp nevű webalkalmazás objektum-hivatkozásának létrehozásához.
Az objektum hivatkozása $WebApp nevű változóban tárolódik.
A második parancs az Object Reference és az **Remove-AzWebAppSSLBinding** parancsmagot használja az SSL-kötés eltávolításához.

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

### -DeleteCertificate
Azt a műveletsort adja meg, amelyet akkor kell végrehajtani, ha az SSL-kötés megszűnt a tanúsítvány által használt egyetlen kötés.
Ha a *DeleteCertificate* értéke $false, a program nem törli a tanúsítványt a kötés törlésekor.
Ha a *DeleteCertificate* értéke $TRUE vagy nem szerepel a parancsban, a tanúsítványt az SSL-kötéssel együtt törli a rendszer.
A tanúsítvány csak akkor törlődik, ha az SSL-kötés megszűnt a tanúsítvány által használt egyetlen kötés.
Ha a tanúsítvány több kötéssel rendelkezik, akkor a tanúsítvány nem törlődik, függetlenül a *DeleteCertificate* paraméter értékétől.

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
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -Name (név)
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
Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.
A *ResourceGroupName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.

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
A Web App telepítő bővítőhelyét adja meg.
Ha egy központi telepítő bővítőhelyet szeretne használni, használja az Get-AzWebAppSlot parancsmagot.

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
Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzWebApp parancsmagot.
A *WebApp* paraméter nem használható ugyanabban a parancsban, mint a *ResourceGroupName* paraméter és/vagy a *WebAppName*.

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
A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. WebApps. models. PSSite

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Új – AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


