---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843901"
---
# Add-AzKeyVaultManagedStorageAccount

## Áttekintés
Hozzáad egy meglévő Azure-tárterületet a megadott kulcs boltozatához a Key Vault szolgáltatás által felügyelt kulcsok számára.

## SZINTAXISA

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Egy meglévő Azure-tárterületet állít be a fő boltozattal a tároló fiók kulcsaival. A tárterület-fióknak már léteznie kell. A tárolási kulcsokat a hívó nem érheti el.
A Key Vault automatikusan újragenerálja és átváltja az aktív kulcsot a megújulási időszak alapján.

## Példák

### 1. példa: az Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

A Key Vault által felügyelt kulcsokat tároló fiókot állít be. Az aktív kulcs a "key1". Ez a kulcs a sas-tokenek generálásához használható. A kulcsfájl a parancs időpontjában a parancs időpontjában a regeneráció után újragenerálja a "azonosító2" billentyűt, majd aktív kulcsként adja meg. Az automatikus regenerálási folyamat továbbra is az "key1" és a "azonosító2" között fog folytatódni a 90 napok közötti eltéréssel.

### 2. példa: a klasszikus Azure Storage-fiók beállítása a Key Vault segítségével a kulcsok kezeléséhez
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

Klasszikus tárolási fiókot állít be a fő boltozattal a kulcsok kezeléséhez. Az aktív kulcs az "elsődleges" érték. Ez a kulcs a sas-tokenek generálásához használható. A kulcs-boltozat a parancs időpontjában a második kulcs után újragenerálja a "másodlagos" billentyűt, majd aktív kulcsként adja meg. Ez az automatikus regenerálási folyamat az "elsődleges" és a "másodlagos" között az 90 napok közötti eltérést követően folytatódik.

## PARAMÉTEREK

### -AccountName
Fontos: a boltozattal felügyelt tárolási fiók neve. Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AccountResourceId
A tárolási fiók Azure erőforrás-azonosítója.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Annak a tárterület-fióknak a neve, amelyet a sas-tokenek generálásához kell használni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Letiltása
Letiltja a felügyelt tárterület-fiók kulcsát a sas-tokenek generálásához.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutoRegenerateKey
Automatikus újragenerálási kulcs. Ha igaz, akkor a felügyelt tárterület-fiók inaktív kulcsa automatikusan újra létrejön, és a regeneráció után válik az új aktív kulcs. Ha hamis, akkor a felügyelt tárterület fiók kulcsait nem kell automatikusan újragenerálni.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegenerationPeriod
A regeneráció időszaka Ha az automatikus újragenerálási kulcs engedélyezve van, ez az érték határozza meg azt a időszak, amely után a felügyelt tárolási fiók inaktív kulcsát újra létrehozta a rendszer, és az új aktív kulcs lesz.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Boltozat neve.
A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. ManagedStorageAccount. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Az.-boltozat](/powershell/module/Az.keyvault)
