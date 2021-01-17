---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469529"
---
# Set-AzKeyVaultManagedStorageSasDefinition

## SYNOPSIS
Egy megosztott hozzáférés-aláírás (SAS) definícióját állítja be egy adott, kulcstárolóval felügyelt Azure Storage-fiók kulcstárával.

## SZINTAXIS

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

## LEÍRÁS
Megosztott hozzáférés-aláírás (SAS) definícióját állítja be egy adott kulcstároló által felügyelt Azure Storage-fiókkal. Ez egy olyan titkos halmazt is beállítja, amellyel be lehet szerezni az SAS-jogkivonatot ebben az SAS-definícióban.
Az SAS-jogkivonat generálása ezekkel a paraméterekkel és a kulcstároló által felügyelt Azure Storage-fiók aktív kulcsával jön létre.

## PÉLDÁK

### 1. példa: Fióktípusú SAS-definíció beállítása és az alapján aktuális SAS-jogkivonat beszerzése
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

Egy "mykv" tárolóban egy KeyVault-felügyelt tárfiók "mysa" szolgáltatásában beállítja a fiók SAS-definíciójának "accountsas" beállítását. Konkrétan a fenti sorozat az alábbi műveleteket végzi el:
  - (meglévő) tárfiókot kap
  - kap egy (meglévő) kulcstárat
  - hozzáad egy KeyVault-kezelt tárfiókot a tárolóhoz, a Kulcs1 értéket aktív kulcsként 180 napos időszakkal megszabadítva
  - beállítja a tárterület környezetét a megadott tárfiókhoz a Kulcs1 billentyűvel
  - létrehoz egy fiók SAS-jogkivonatot a szolgáltatások blobjának, fájljának, táblázatának és várólistájának, az erőforrástípusok szolgáltatásának, tárolójának és objektumának, az összes engedélyével a https protokollon keresztül, valamint a megadott kezdési és befejezési dátummal
  - Egy KeyVault-kezelt tároló SAS-definíciót állít be a tárolóban úgy, hogy a fent létrehozott SAS-tokenként a uri sablon "fiók" típusú, és 30 napig érvényes legyen
  - Lekéri a tényleges hozzáférési jogkivonatot az SAS-definíciónak megfelelő KeyVault-titkos kulcsból

## PARAMETERS

### -AccountName
Key Vault managed storage account name. A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tárolónévből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből.

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

### -Disable
Letiltja a sas-definíció használatát a sas tokenek generálásához.

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

### -Name
Tárterület sas-definíciójának neve. A parancsmag egy tárolónévből ( jelenleg kijelölt környezetből, tárfiók neve és sas-definíció neve) származó tár sas-definíciójának teljes tartománynevét építi fel.

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
Tárterület SAS-típusa.

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

### -Tag
Kulcsérték-párok kivonattábla formájában. Például: @{key0="érték0";key1=$null;key2="érték2"}

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
Storage SAS-definíciós sablon uri.

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
A sas token lejárati idejének a generálástól való beállításakor használt érvényességi idő

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
Tároló neve.
A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azureâ€™RM.â€](/powershell/module/az.keyvault/)
