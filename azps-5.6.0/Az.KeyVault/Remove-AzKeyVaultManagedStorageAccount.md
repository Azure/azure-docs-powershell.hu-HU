---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918873"
---
# Remove-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Eltávolít egy kulcstár által felügyelt Azure Storage-fiókot és az összes hozzá tartozó SAS-definíciót.

## SZINTAXIS

### ByDefinitionName (alapértelmezett)
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
Egy Azure-tárfiók társításának megszava a kulcstárolóból. Ez nem távolít el egy Azure-tárfiókot, hanem eltávolítja a fiókkulcsokat az Azure-kulcstárból. Az összes társított kulcstár felügyelt TÁROLÓ SAS-definíciója is törlődik.

## PÉLDÁK

### 1. példa: Távolítsa el a kulcstár által felügyelt Azure Storage-fiókot és az összes hozzá tartozó SAS-definíciót.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Leállítja az Azure Storage-fiók "mystorageaccount" társítását a myvault kulcstárból, és leállítja a kulcstár kulcskezelését. A rendszer nem távolítja el a "mystorageaccount" fiókot. Az ezzel a fiókkal társított összes kulcstár által felügyelt TÁROLÓ SAS-definíció el lesz távolítva.

### 2. példa: Felhasználói jóváhagyás nélkül távolítson el egy kulcstár által felügyelt Azure Storage-fiókot és az összes hozzá tartozó SAS-definíciót.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Leállítja az Azure Storage-fiók "mystorageaccount" társítását a myvault kulcstárból, és leállítja a kulcstár kulcskezelését. A rendszer nem távolítja el a "mystorageaccount" fiókot. Az ezzel a fiókkal társított összes kulcstár által felügyelt TÁROLÓ SAS-definíció el lesz távolítva.

### 3. példa: Véglegesen töröljön (véglegesen töröljön) egy kulcstár által felügyelt Azure Storage-fiókot és az összes kapcsolódó SAS-definíciót egy soft-delete-enabled tárolóból.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

A példa feltételezi, hogy a szoftveres törlés engedélyezve van ehhez a tárolóhoz. Ellenőrizze, hogy ez a helyzet-e a tároló tulajdonságainak vagy a tárolóban egy entitás RecoveryLevel attribútumának vizsgálatával.
Az első parancsmag leállítja az Azure Storage-fiók "mystorageaccount" társítását a "myvault" kulcstárból, és leállítja a kulcstár kulcskezelését. A rendszer nem távolítja el a "mystorageaccount" fiókot. Az ezzel a fiókkal társított összes kulcstár által felügyelt TÁROLÓ SAS-definíció el lesz távolítva.
A második parancsmag ellenőrzi, hogy a tárfiók törölt, de helyreállítható állapotban van-e. Ennek az állapotnak a elérése némi időt igényel, engedélyezze a ~30s-et a próbálkozás előtt.
A harmadik parancsmag véglegesen eltávolítja a tárfiókot – a helyreállítás már nem lehetséges.

## PARAMETERS

### -AccountName
Key Vault managed storage account name. A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tárolónévből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Ne kérjen megerősítést.

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
ManagedStorageAccount objektum.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Távolítsa el véglegesen a korábban törölt felügyelt tárfiókot.

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

### -PassThru
A parancsmag alapértelmezés szerint nem ad vissza objektumot.
Ha ez a kapcsoló meg van adva, a parancsmag a törölt felügyelt tárfiókot adja vissza.

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
Tároló neve.
A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## KIMENETEK

### Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageAccount

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

