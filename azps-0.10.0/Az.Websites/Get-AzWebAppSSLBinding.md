---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842773"
---
# Get-AzWebAppSSLBinding

## Áttekintés
Az Azure Web App tanúsítványának SSL-kötését kapja.

## SZINTAXISA

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzWebAppSSLBinding** parancsmag Secure Sockets Layer (SSL) kötést kap az Azure Web App alkalmazáshoz.
Az SSL-kötések a webalkalmazások feltöltött tanúsítványsal való társítására szolgálnak.
A webes alkalmazások több tanúsítványhoz is kötve lehetnek.

## Példák

### Példa 1: SSL-kötések beszerzése egy webalkalmazáshoz
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Ez a parancs beolvassa a Web App ContosoWebApp az erőforráscsoport ContosoResourceGroup társított SSL-kötéseit.

### 2. példa: az SSL-kötések beszerzése egy webalkalmazáshoz objektum-hivatkozás használatával
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Az ebben a példában szereplő parancsok a Web App ContosoWebApp tartozó SSL-kötéseket is megkapják; Ebben az esetben azonban a Web App neve és a hozzá tartozó erőforráscsoport neve helyett egy objektum-hivatkozás van használatban.
Ezt az objektumot a példa első parancsa hozza létre, amely a **Get-AzWebApp** használatával hozza létre az objektum hivatkozását a ContosoWebApp nevű webalkalmazáshoz.
Az objektum hivatkozása $WebApp nevű változóban tárolódik.

Ezt a változót és a **Get-AzWebAppSSLBinding** parancsmagot a második parancs használja az SSL-kötések beszerzéséhez.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az SSL-kötés nevét adja meg.

```yaml
Type: String
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
Type: String
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
Ha egy központi telepítő bővítőhelyet szeretne használni, használja az Get-AzWebAppSlot parancsmagot.

```yaml
Type: String
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

```yaml
Type: Site
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
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Webhely
A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


