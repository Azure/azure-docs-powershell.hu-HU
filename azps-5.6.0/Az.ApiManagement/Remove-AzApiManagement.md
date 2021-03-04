---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: daa4169ed077003d2ceb773e2e085e72fb6d1ec8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922193"
---
# Remove-AzApiManagement

## SYNOPSIS
Eltávolít egy API-kezelési szolgáltatást.

## SZINTAXIS

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzApiManagement** parancsmag eltávolítja az Azure API Management szolgáltatást.

## PÉLDÁK

### 1. példa: API-kezelési szolgáltatás eltávolítása
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

Ez a parancs eltávolítja a ContosoApi nevű API-kezelési szolgáltatást.

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
Annak az API Management-telepítésnek a nevét adja meg, amelyről ez a parancsmag eltávolítja.

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

### -PassThru
Azt jelzi, hogy ha a művelet sikeres, a parancsmag $True értéket ad vissza.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amely alatt az API-kezelési telepítés létezik.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzApiManagement](./Backup-AzApiManagement.md)

[Get-AzApiManagement](./Get-AzApiManagement.md)

[New-AzApiManagement](./New-AzApiManagement.md)

[Restore-AzApiManagement](./Restore-AzApiManagement.md)


