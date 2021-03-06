---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: ae03fd4dedf1e0e6de91bd036180379c2be2cabe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494589"
---
# Get-AzureRmWebAppSSLBinding

## Áttekintés
Az Azure Web App tanúsítványának SSL-kötését kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### S1
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmWebAppSSLBinding** parancsmag Secure Sockets Layer (SSL) kötést kap az Azure Web App alkalmazáshoz.
Az SSL-kötések a webalkalmazások feltöltött tanúsítványsal való társítására szolgálnak.
A webes alkalmazások több tanúsítványhoz is kötve lehetnek.

## Példák

### Példa 1: SSL-kötések beszerzése egy webalkalmazáshoz
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Ez a parancs beolvassa a Web App ContosoWebApp az erőforráscsoport ContosoResourceGroup társított SSL-kötéseit.

### 2. példa: az SSL-kötések beszerzése egy webalkalmazáshoz objektum-hivatkozás használatával
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

Az ebben a példában szereplő parancsok a Web App ContosoWebApp tartozó SSL-kötéseket is megkapják; Ebben az esetben azonban a Web App neve és a hozzá tartozó erőforráscsoport neve helyett egy objektum-hivatkozás van használatban.
Ezt az objektumot a példa első parancsa hozza létre, amely a **Get-AzureRmWebApp** használatával hozza létre az objektum hivatkozását a ContosoWebApp nevű webalkalmazáshoz.
Az objektum hivatkozása $WebApp nevű változóban tárolódik.

Ezt a változót és a **Get-AzureRmWebAppSSLBinding** parancsmagot a második parancs használja az SSL-kötések beszerzéséhez.

## PARAMÉTEREK

### -Name (név)
Az SSL-kötés nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
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
Egy webalkalmazás-telepítő bővítőhelyet ad meg.
Ha egy központi telepítő bővítőhelyet szeretne használni, használja az Get-AzureRMWebAppSlot parancsmagot.

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
Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzureRmWebApp parancsmagot.

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Annak a webalkalmazásnak a nevét adja meg, amelynek a parancsmagja SSL-kötést kap.

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

[Új – AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


