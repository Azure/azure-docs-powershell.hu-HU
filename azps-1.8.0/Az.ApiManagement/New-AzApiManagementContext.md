---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671675"
---
# New-AzApiManagementContext

## Áttekintés
Létrehozza a PsAzureApiManagementContext példányát.

## SZINTAXISA

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzApiManagementContext** parancsmag a **PsAzureApiManagementContext** példányát hozza létre.
A környezet az API-kezelési szolgáltatás összes parancsmagja esetén használatos.

## Példák

### 1. példa: PsApiManagementContext-példány létrehozása
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

Ez a parancs létrehoz egy **PsApiManagementContext** -példányt.

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

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amely alatt egy API-kezelési szolgáltatás van telepítve.

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

### -Szolgáltatásnév
A telepített API-kezelési szolgáltatás nevét adja meg.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
