---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: 393b811ec7bc2d7a3ddafda3a33b5460e4bef6dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469221"
---
# Disable-AzContextAutosave

## SYNOPSIS
Kapcsolja ki az Azure-beli hitelesítő adatok automatikus mentését.  A bejelentkezési adatok a PowerShell-ablak következő megnyitásakor elfelejtkednek

## SZINTAXIS

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Kapcsolja ki az Azure-beli hitelesítő adatok automatikus mentését.  A bejelentkezési adatok a PowerShell-ablak következő megnyitásakor elfelejtkednek

## PÉLDÁK

### 1. példa: A környezet automatikus mentésének letiltása
```powershell
PS C:\> Disable-AzContextAutosave
```

Tiltsa le az automatikus mentést az aktuális felhasználó számára.

### 2. példa

Kapcsolja ki az Azure-beli hitelesítő adatok automatikus mentését ebben a PowerShell-munkamenetben. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Disable-AzContextAutosave -Scope Process
```

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés

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

### -Scope
Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
