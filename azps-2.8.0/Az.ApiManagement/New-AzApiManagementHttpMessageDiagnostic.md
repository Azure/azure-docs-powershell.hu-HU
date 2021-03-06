---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 89e7ffd1931f3aa4170656d7846e3e370baf2864
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668042"
---
# New-AzApiManagementHttpMessageDiagnostic

## Áttekintés
A **PsApiManagementHttpMessageDiagnostic** egy példányát hozza létre, amely a diagnosztikai rendszer http-üzenet diagnosztikai beállítása

## SZINTAXISA

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzApiManagementHttpMessageDiagnostic** parancsmag a http-üzenet diagnosztikai beállítását hozza létre.

## Példák

### Példa 1: alapvető http-üzenet diagnosztikai beállításainak létrehozása
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

Http-üzenet diagnosztikai beállításának létrehozása a naplózás `Content-Type` és a `User-Agent` fejlécek 100 bájtjaival együtt `body`

## PARAMÉTEREK

### -BodyBytesToLog
A naplózni kívánt beolvasási törzs bájtjainak száma. Ez a paraméter nem kötelező.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -HeadersToLog
A naplózni kívánt fejlécek sora. Ez a paraméter nem kötelező.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementHttpMessageDiagnostic

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzApiManagementDiagnostic](./New-AzApiManagementDiagnostic.md)

[Új – AzApiManagementSamplingSetting](./New-AzApiManagementHttpMessageDiagnostic.md)