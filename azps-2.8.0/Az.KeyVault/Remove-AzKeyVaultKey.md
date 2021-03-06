---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: afa9f59520cba9f90f0f5d0a2edb6564b73245bf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406145"
---
# Remove-AzKeyVaultKey

## SYNOPSIS
Kulcs törlése egy kulcstárban.

## SZINTAXIS

### ByVaultName (alapértelmezett)
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A Remove-AzKeyVaultKey parancsmag törli a kulcsot a kulcstárból.
Ha a kulcsot véletlenül törölték, a kulcsot a speciális "helyreállításUndo-AzKeyVaultKeyRemoval engedéllyel rendelkező felhasználó helyreállíthatja.
Ez a parancsmag a **ConfirmImpact** tulajdonság értéke magas.

## PÉLDÁK

### 1. példa: Kulcs eltávolítása egy kulcstárból
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

Ez a parancs eltávolítja az ITSoftware nevű kulcsot a Contoso nevű kulcstárból.

### 2. példa: Kulcs eltávolítása a felhasználó jóváhagyása nélkül
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

Ez a parancs eltávolítja az ITSoftware nevű kulcsot a Contoso nevű kulcstárból.
A parancs megadja a *Force* paramétert, ezért a parancsmag nem kér megerősítést.

### 3. példa: Törölt kulcs végleges törlése a kulcstárból
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

Ez a parancs véglegesen eltávolítja az ITSoftware nevű kulcsot a Contoso nevű kulcstárból.
A parancsmag végrehajtatása "végleges végleges" engedélyt igényel, amelyet korábban és kifejezetten a felhasználónak adott meg ehhez a kulcstárhoz.

### 4. példa: Kulcsok eltávolítása a folyamat műveleti operátorával
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

Ez a parancs a Contoso nevű kulcstár összes kulcsát beveszi, és a folyamat műveleti operátorával átadja őket a **Where-Object** parancsmagnak.
Ez a parancsmag átadja az Engedélyezett $False értékkel  rendelkező kulcsokat az aktuális parancsmagnak.
Ez a parancsmag eltávolítja ezeket a kulcsokat.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Force
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

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

### -InputObject
KeyBundle objektum

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Távolítsa el véglegesen a korábban törölt kulcsot.

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

### -Name
Az eltávolítható kulcs neve.
Ez a parancsmag egy kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstár neve és az aktuális környezet alapján.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Azt jelzi, hogy ez a parancsmag **egy Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey objektumot ad** vissza.
Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.

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

### -VaultName
Annak a kulcstárnak a nevét adja meg, amelyből el szeretné távolítani a kulcsot.
Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## KIMENETEK

### Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKey billentyű

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)


[Undo-AzKeyVaultKeyRemoval](./Undo-AzKeyVaultKeyRemoval.md)

