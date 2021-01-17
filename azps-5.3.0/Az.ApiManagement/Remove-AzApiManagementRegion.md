---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381931"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
Eltávolít egy meglévő telepítési régiót a PsApiManagement-példányból.

## SZINTAXIS

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzApiManagementRegion** parancsmag eltávolítja a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** típusú példányokat az **AdditionalRegions** gyűjteményből, feltéve hogy a **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
Ez a parancsmag nem módosítja a telepítést önmagában, de frissíti a **PsApiManagement** in-memory példányát.
Az API-felügyelet telepítésének frissítéséhez adja át a **módosított PsApiManagementInstance-t** a **Set-AzApiManagementnek.**

## PÉLDÁK

### 1. példa: Régió eltávolítása a PsApiManagement-példányból
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Ez a parancs eltávolítja az Egyesült Államok keleti régióját a **PsApiManagement-példányból.**

### 2. példa: Terület eltávolítása a PsApiManagement-példányból parancssorozat használatával
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Ez az első parancs a ContosoApi nevű erőforráscsoport **PsApiManagement** példányát kapja.
Az utolsó parancs ezután eltávolítja az Egyesült Államok keleti régióját a példányból, majd frissíti az üzembe helyezést.

## PARAMETERS

### -ApiManagement
Azt a **PsApiManagement-példányt** adja meg, amelyből a parancsmag eltávolítja a további telepítési régiót.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile

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

### -Location
Megadja annak a területnek a helyét, amelyről a parancsmag eltávolítja.
Megadja az új telepítési régió helyét az Api Management szolgáltatás által támogatott régió között.
Érvényes helyek beszerzéséhez használja a Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" parancsmagot | ahol {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object helyek

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


