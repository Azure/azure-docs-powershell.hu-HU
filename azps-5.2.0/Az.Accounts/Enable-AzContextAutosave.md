---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370872"
---
# Enable-AzContextAutosave

## SYNOPSIS
Az Azure környezetei olyan PowerShell-objektumok, amelyek az aktív előfizetést képviselik, amelyeken parancsokat futtathat, valamint az Azure-felhőhöz való csatlakozáshoz szükséges hitelesítési adatok. Az Azure-környezetek esetén az Azure PowerShellnek nem kell minden alkalommal újra hitelesenie a fiókját, amikor előfizetést vált. További információért lásd az [Azure PowerShell környezetobjektumokat.](https://docs.microsoft.com/powershell/azure/context-persistence)

Ez a parancsmag lehetővé teszi az Azure környezetinformációk mentését és automatikus betöltéset a PowerShell-folyamat elindítani. Új ablak megnyitásakor például.

## SZINTAXIS

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS

Lehetővé teszi az Azure környezetinformációk mentését és automatikus betöltését a PowerShell-folyamat indításakor. A környezet a környezetre befolyásoló parancsmagok végrehajtásának végén lesz mentve. Bármely profil-parancsmagot például. Ha felhasználói hitelesítést használ, a parancsmagok futtatása során a jogkivonatok frissíthetők.

## PÉLDÁK

### 1. példa: A hitelesítő adatok automatikus mentésének engedélyezése az aktuális felhasználónál

Kapcsolja be a hitelesítő adatok automatikus mentését az aktuális felhasználó számára. Amikor megnyit egy PowerShell-ablakot, a rendszer bejelentkezés nélkül emlékezni fog az aktuális környezetre.

```powershell
Enable-AzContextAutosave
```

### 2. példa

Az Azure-beli hitelesítő adatok, fiókok és előfizetési adatok mentésének és automatikus betölt használatának engedélyezése, amikor ebben a PowerShell-munkamenetben megnyit egy PowerShell-ablakot. (automatikusan generált)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
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

Meghatározza a környezetváltozások hatókörét. Például az, hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e. A hatókörrel végrehajtott módosítások minden, a felhasználó által `CurrentUser` elindított PowerShell-munkamenetre hatással lesznek. Ha egy adott munkamenetnek más beállításokra van szüksége, használja a `Process` hatókört.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
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

### Gyakori paraméterek

Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
