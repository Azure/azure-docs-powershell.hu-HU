---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: fadf6b15eb25f07d88254a5d3a998f1692e5cf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679764"
---
# Remove-AzureKeyVaultManagedStorageSasDefinition

## Áttekintés
Eltávolítja az Azure Managed Azure Storage SAS definícióit.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Eltávolítja az Azure Managed Azure Storage SAS definícióit. Ez a beállítás eltávolítja azt a titkot is, amellyel a SAS-tokent a SAS-definícióval szerezheti be.

## Példák

### Példa 1: az Azure Managed Azure Storage SAS definíciójának eltávolítása.
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.

### 2. példa: távolítsa el a Key Vault Managed Azure Storage SAS definícióját felhasználó megerősítés nélkül.
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.

## PARAMÉTEREK

### -AccountName
Tárolási fiók neve.
Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a boltozat neve, a jelenleg kijelölt környezet és a tárolási fiók neve között.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name (név)
Storage sas-definíció neve.
Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. ManagedStorageSasDefinition. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

