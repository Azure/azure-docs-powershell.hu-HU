---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://go.microsoft.com/fwlink/?LinkId=690299
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: b5f2917da71e8c4539660dbb91dd81f3fb5d7959
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502715"
---
# Remove-AzureKeyVaultKey

## Áttekintés
Billentyűt töröl a kulcs boltozatáról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A Remove-AzureKeyVaultKey parancsmag egy billentyűt töröl a kulcs-boltozatban.
Ha a kulcsot véletlenül töröltük, a kulcs visszaállítható a Undo-AzureKeyVaultKeyRemoval felhasználó által speciális "helyreállítási" engedélyekkel.
A parancsmag értéke magas a **ConfirmImpact** tulajdonság számára.

## Példák

### 1. példa: kulcs eltávolítása a főboltozatról
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.

### 2. példa: kulcs eltávolítása a felhasználó jóváhagyása nélkül
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso nevű kulcsból.
A parancs az *erő* és a *megerősítés* paramétert adja meg, ezért a parancsmag nem kér megerősítést.

### 3. példa: a törölt billentyűk végleges kiürítése a kulcs boltozatáról
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

Ez a parancs eltávolítja a ITSoftware nevű kulcsot a contoso állandóról.
A parancsmag végrehajtásához a "Purge" engedély szükséges, amelyet előzőleg és kifejezetten meg kell adni a felhasználónak a kulcs boltozatához.

### 4. példa: kulcsok eltávolítása a csővezeték-kezelő használatával
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

Ez a parancs a contoso nevű kulcs-boltozat összes kulcsát beolvassa, és a pipeline operátor segítségével átadja őket a **Where-Object** parancsmagnak.
Ez a parancsmag átadja azokat a kulcsokat, amelyek $False értékkel rendelkeznek az **engedélyezett** attribútumhoz az aktuális parancsmaghoz.
A parancsmag eltávolítja ezeket a billentyűket.

## PARAMÉTEREK

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -InRemovedState
A korábban törölt kulcs végleges eltávolítása.

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
Az eltávolítandó kulcs nevét adja meg.
Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Azt jelzi, hogy ez a parancsmag a **Microsoft. Azure. commands.-Vault. models. Bundle** objektumot adja eredményül.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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
Annak a kulcsnak a nevét adja meg, amelyből el szeretné távolítani a billentyűt.
Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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

### Karakterlánc

## KIMENETEK

### Microsoft. Azure. Command. DeletedKeyBundle. models.
Ez a parancsmag csak akkor ad értéket, ha a *PassThru* paramétert adja meg.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

[Visszavonás – AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

