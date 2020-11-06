---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 99d7d4a0feeb0f548ef65d06234eecb1ad2baf6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504671"
---
# New-AzureRmWebAppSSLBinding

## Áttekintés
Az Azure Web App-hoz létrehoz egy SSL-tanúsítványt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### S1
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmWebAppSSLBinding** parancsmag létrehoz egy Secure Socket Layer (SSL) tanúsítvány-kötést az Azure Web App alkalmazáshoz.
A parancsmag két módon hoz létre SSL-kötést: 

- Egy webalkalmazást meglévő tanúsítványhoz köthet le.
- Feltöltheti az új tanúsítványt, majd az új tanúsítványhoz rögzítheti a webalkalmazást.

Attól függetlenül, hogy melyik módszert használja, a tanúsítványnak és a webalkalmazásnak ugyanahhoz az Azure-erőforrás csoporthoz kell tartoznia.
Ha van egy webalkalmazása az A erőforráscsoport-ban, és a webalkalmazást egy, a B erőforrás csoportba tartozó tanúsítványba szeretné kötni, az egyetlen mód arra, hogy a tanúsítvány másolatát feltöltse az A erőforrás csoportba.

Új tanúsítvány feltöltése esetén tartsa szem előtt az alábbi követelményeket az Azure SSL-tanúsítványok esetében: 

- A tanúsítványnak tartalmaznia kell egy titkos kulcsot. 
- A tanúsítványnak a személyes adatok cseréje (PFX) formátumát kell használnia. 
- A tanúsítvány tulajdonosának nevének egyeznie kell a webalkalmazás eléréséhez használt tartománnyal. 
- A tanúsítványnak legalább 2048 bites titkosítást kell használnia.

## Példák

### 1. példa: tanúsítvány kötése webalkalmazáshoz
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd"
```

Ez a parancs egy meglévő Azure-tanúsítványt (az ujjlenyomat-E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 tartalmazó tanúsítványt) köti össze a ContosoWebApp nevű webalkalmazással.

### 2. példa: tanúsítvány feltöltése és webalkalmazáshoz kötése
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd" -CertificateFilePath "C:\Certificates\ContosoWebSite.pfx"
```

Példa: a E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 az ContosoWebApp nevű webalkalmazáshoz is köti a tanúsítványt.
Ebben az esetben azonban a tanúsítvány még nincs feltöltve az Azure-ra.
Emiatt a *CertificateFilePath* paraméter a tanúsítvány helyi példányának megadására szolgál. PFX-fájl.
Ezt a tanúsítványt az Azure-ra tölti fel a rendszer, majd létrejön az új SSL-kötések.

## PARAMÉTEREK

### -CertificateFilePath
A feltölteni kívánt tanúsítvány elérési útvonalát adja meg.

A *CertificateFilePath* paraméter csak akkor szükséges, ha a tanúsítvány még nincs feltöltve az Azure-ra.

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
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
A webalkalmazás-telepítő bővítőhely nevét adja meg.
A Get-AzureRMWebAppSlot parancsmaggal letölthet egy bővítőhelyet.

A telepítő bővítőhelyek segítségével a webes alkalmazások csak akkor érhetők el, ha az alkalmazások nem érhetők el az interneten keresztül.
Általában a módosításokat egy átmeneti webhelyre telepíti, érvényesíti ezeket a módosításokat, majd üzembe helyezi a termelés (internetről elérhető) webhelyre.

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
Megadja, hogy engedélyezve van-e a tanúsítvány.
Állítsa a *SSLState* paramétert 1-re a tanúsítvány engedélyezéséhez, vagy állítsa a *SSLState* 0-ra a tanúsítvány letiltásához.

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

### -Ujjlenyomat
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
Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzureRmWebApp parancsmagot.

A *WebApp* paraméter nem használható ugyanabban a parancsban, mint a *ResourceGroupName* paraméter és/vagy a *WebAppName*.

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Annak a webalkalmazásnak a nevét adja meg, amelyhez az új SSL-kötést létrehozta.

A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Webhely
A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


