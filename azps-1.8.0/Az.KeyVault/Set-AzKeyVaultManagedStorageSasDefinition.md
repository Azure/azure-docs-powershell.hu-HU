---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 65aeede664e0817bbc3465721a14580bd897d1f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835653"
---
# Set-AzKeyVaultManagedStorageSasDefinition

## Áttekintés
Megosztott hozzáférés-aláírást (SAS) állít be a fő boltozattal egy adott kulcs boltozattal felügyelt Azure Storage-fiókkal.

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Megosztott hozzáférés-aláírást (SAS) állít be egy adott kulcsos, felügyelt Azure tárterület-fiókkal. Ez azt is megadhatja, hogy milyen titok használható a SAS-token beszerzéséhez a SAS-definícióban.
A SAS-token az alábbi paraméterekkel és a Key Vault Managed Azure Storage Account aktív kulcsával jön létre.

## Példák

### Példa 1: fiók típusú SAS-definíció beállítása, és a jelenlegi biztonsági társítási jogkivonat beolvasása az alapján
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

Egy "accountsas" fiókját egy "mysa" "mykv" tárolóban, a "". A fenti sorrend konkrétan a következőket hajtja végre:
  - egy (meglévő) tárterület-fiókot kap
  - beolvassa a (korábbi) kulcs boltozatát
  - egy kulcskezelő által felügyelt tárolási fiók hozzáadása a boltozathoz, a Key1 beállítása aktív kulcsként, valamint a 180 napok regenerálási időszaka
  - tárolási környezet beállítása a megadott tárterület-fiókhoz a Key1 használatával
  - a fiókhoz tartozó SAS-tokent hoz létre a szolgáltatások Blobja, a fájl, a táblázat és a várólista, az erőforrástípusok szolgáltatáshoz, a tárolóhoz és az objektumhoz, az összes engedély, a https és a megadott kezdési és befejezési dátum
  - a boltozattal felügyelt tárterület biztonsági társítását állítja be a Vault-ban, és a sablon URI-ja a fenti néven létrehozott SAS-token, a "fiók" vagy 30 napig érvényes
  - beolvassa a tényleges hozzáférési jogkivonatot a biztonsági társítás definíciójának megfelelő kulcsból.

## PARAMÉTEREK

### -AccountName
Fontos: a boltozattal felügyelt tárolási fiók neve. Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

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

### -Letiltása
Letiltja a sas-definíció használatát a sas-token generálásához.

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

### -Name (név)
Storage sas-definíció neve. Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasType
Storage SAS típus.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateUri
Tárolási SAS-definíciós sablon URI-ja

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidityPeriod
Annak az érvényességi időszaknak a meghatározása, amely a sas-token lejárati időpontjának a generált időponttól való beállításához használatos.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
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
Parameter Sets: Default
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

### Microsoft. Azure. Command. PSKeyVaultManagedStorageSasDefinition. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azureâ € ‹ RM. â € ‹ keyĂ € ‹ Vault](/powershell/module/az.keyvault/)
