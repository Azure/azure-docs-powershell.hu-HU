---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 38af48c1f7b5ae8eb4a3be0f5b2fea6fbe452f0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666166"
---
# Remove-AzKeyVaultManagedStorageAccount

## Áttekintés
A felügyelt Azure Storage-fiók és az összes társított biztonsági társítási definíció eltávolítása.

## SZINTAXISA

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

## Leírás
Az Azure Storage-fiók társítása a Key Vault-ról Ez a művelet nem távolítja el az Azure-tárterületet, de eltávolítja a fiók kulcsait az Azure Key Vault által felügyelt fiókból. Az összes társított kulcs boltozata: a biztonsági társítások definíciója is törlődik.

## Példák

### 1. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót.
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

Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről. Nem törlődik a "mystorageaccount" fiók. A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.

### 2. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót felhasználó megerősítés nélkül.
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

Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről. Nem törlődik a "mystorageaccount" fiók. A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.

### 3. példa: a fontos, az Azure által felügyelt fő tároló-fiók és az összes társított biztonsági társítási definíció végleges törlése (kiürítése).
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

A példa feltételezi, hogy a boltozathoz engedélyezve van a finom törlés. Ellenőrizze, hogy ez-e a helyzet a boltozat tulajdonságainak vagy a RecoveryLevel attribútumának a boltozatban való vizsgálatával.
Az első parancsmag az Azure-tárterület "mystorageaccount"-fiókját nem társítja a "myvault" kulccsal, és a kulcs-boltozatot leállítja a kulcsok kezeléséhez. Nem törlődik a "mystorageaccount" fiók. A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.
A második parancsmag azt ellenőrzi, hogy a tárolási fiók törölt, de helyreállítható állapotban van-e. Ha elérte ezt az állapotot, akkor szükség lehet némi időre, kérjük, hogy próbálkozzon a ~ 30-as évekkel.
A harmadik parancsmag véglegesen eltávolítja a tárterület-helyreállítási fiókot, a továbbiakban nem lesz lehetséges.

## PARAMÉTEREK

### -AccountName
Fontos: a boltozattal felügyelt tárolási fiók neve. Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
ManagedStorageAccount objektum

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
Véglegesen eltávolítja a korábban törölt távtárolású tárterület-fiókot.

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
Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.

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
Boltozat neve.
A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.

## KIMENETEK

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

