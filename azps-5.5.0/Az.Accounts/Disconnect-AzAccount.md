---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145362"
---
# Disconnect-AzAccount

## SYNOPSIS
Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókkal társított összes hitelesítő adatokat és kontextust.

## SZINTAXIS

### ContextName (alapértelmezett)
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UserId
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipal
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContextObject
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A Disconnect-AzAccount parancsmag leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókhoz társított összes hitelesítő adatokat és kontextust (előfizetési és bérlői adatokat).
A parancsmag végrehajtása után újból be kell jelentkeznie a Connect-AzAccount használatával.

## PÉLDÁK

### 1. példa: Kijelentkezés az aktuális fiókból
```powershell
PS C:\> Disconnect-AzAccount
```

Kijelentkezik az aktuális környezethez társított Azure-fiókból.

### 2. példa: Kijelentkezés egy adott környezethez társított fiókból
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

Kijelentkezik a megadott környezethez tartozó ("Munka" nevű) fiókból. Mivel ez a "CurrentUser" hatókört használja, minden hitelesítő adat és környezet véglegesen törlődik.

### 3. példa: Kijelentkezés egy adott felhasználóból
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

Kijelentkezik a " ' felhasználó – a felhasználóhoz társított összes hitelesítő adat és környezet user1@contoso.org törlődik.

## PARAMETERS

### -ApplicationId
ServicePrincipal id (globálisan egyedi azonosító)

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureContext
Környezet

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ContextName
Annak a környezetnek a neve, amelyből ki kell jelentkezni

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject
Az eltávolítható fiókobjektum

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Scope
Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.

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

### -TenantId
Bérlőazonosító (globálisan egyedi azonosító)

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Felhasználónév
Az űrlap felhasználóneve ' user@contoso.org

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
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
A parancsmag nem hajtódik végre.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext

## KIMENETEK

### Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
