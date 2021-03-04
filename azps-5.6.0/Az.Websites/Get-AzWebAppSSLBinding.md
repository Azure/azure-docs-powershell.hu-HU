---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929465"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Azure Web App-tanúsítvány SSL-kötést kap.

## SZINTAXIS

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzWebAppSSLBinding** parancsmag ssl-kötést kap az Azure Web Apphoz.
Az SSL-kötések a webalkalmazások egy feltöltött tanúsítvánnyal való társítását használják.
A webalkalmazások több tanúsítványhoz is kötve lehet.

## PÉLDÁK

### 1. példa: SSL-kötések lekérte webalkalmazáshoz
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Ez a parancs beolvassa a ContosoWebApp webapp SSL-kötését, amely a ContosoResourceGroup erőforráscsoporthoz van társítva.

### 2. példa: Objektumhivatkozás használata a webalkalmazás SSL-kötésének lekértéhez
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

A példában található parancsok a ContosoWebApp webapp SSL-kötését is megkapják; ebben az esetben azonban a webalkalmazás neve és a társított erőforráscsoport neve helyett objektumhivatkozást használ a szolgáltatás.
Ezt az objektumhivatkozást a példa első parancsa hozza létre, amely a **Get-AzWebApp** segítségével létrehoz egy objektumhivatkozást a ContosoWebApp nevű webappra.
Ezt az objektumhivatkozást egy $WebApp.
Ezt a változót és a **Get-AzWebAppSSLBinding** parancsmagot a második parancsmag használja az SSL-kötések be szereznie.

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
Egy webalkalmazás-telepítőhelyet ad meg.
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
Webalkalmazás lekérte a Get-AzWebApp parancsmagot.

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
Annak a webalkalmazásnak a nevét adja meg, amelyből ez a parancsmag SSL-kötéseket kap.
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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## KIMENETEK

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


