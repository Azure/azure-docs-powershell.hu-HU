---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327568"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
Frissíti egy titkos kulcs attribútumát egy kulcstárban.

## SZINTAXIS

### Alapértelmezett (alapértelmezett)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Update-AzKeyVaultSecret** parancsmag frissíti egy kulcstárban található titkos kulcs szerkeszthető attribútumát.

## PÉLDÁK

### 1. példa: Egy titkos attribútum módosítása
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

Az első négy parancs attribútumokat definiál a lejárati dátumhoz, a NotBefore dátumhoz, a címkékhez és a környezettípushoz, és az attribútumokat változókban tárolja.
A végleges parancs módosítja a ContosoVault nevű kulcstárolóBAN található HR nevű kulcs attribútumát a tárolt változók használatával.

### 2. példa: Titkos címkék és tartalomtípus törlése
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Ez a parancs törli a Contoso nevű kulcstárban található HR nevű titkos fájl adott verziójának címkéit és tartalomtípusát.

### 3. példa: A titkos kulcsok aktuális verziójának letiltása, amelynek a neve IT-val kezdődik
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

Az első parancs a Contoso karakterláncértéket tárolja a $Vault változóban.
A második parancs az IT karakterlánc értékét tárolja a $Prefix változóban.
A harmadik parancs a Get-AzKeyVaultSecret parancsmag segítségével begyűjte a megadott kulcstárban található titkosságokat, majd átadja ezeket a titkosságokat a **Where-Object** parancsmagnak. A **Where-Object** parancsmag az IT karakterekkel kezdődik nevek titkos karaktereit szűri. A parancs a szűrőnek megfelelő titkosságokat a Update-AzKeyVaultSecret kapcsolja ki őket.

### 4. példa: A ContentType beállítása egy titkos fájl minden verziójához
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

Az első három parancs karakterlánc-változókat definiál a *VaultName,* a *Name* és a *ContentType paraméterhez.* A negyedik parancs a Get-AzKeyVaultKey parancsmagot használja a megadott kulcsok lekértéséhez, és a Update-AzKeyVaultSecret-parancsmag billentyűivel XML-re állíthatja be a tartalomtípusukat.

## PARAMETERS

### -ContentType
A Secret tartalomtípusa.
Ha nincs megadva, a titkos fájl tartalomtípusának meglévő értéke változatlan marad.
Távolítsa el a meglévő tartalomtípus-értéket egy üres karakterlánc megadásával.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Enable
Ha jelen van, engedélyezzen egy titkos értéket, ha az érték igaz.
Tiltsa le a titkos adatokat, ha az érték hamis.
Ha nincs megadva, a titkos fájl engedélyezett/letiltott állapotának meglévő értéke változatlan marad.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lejár
A titkos idő lejárati ideje az UTC-ben.
Ha nincs megadva, a titkos kulcs lejárati időének meglévő értéke változatlan marad.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Titkos objektum

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Titkos név.
A parancsmag a tárolónévből ( jelenleg kijelölt környezetből és titkos névből ) egy titkos kulcs teljes tartománynevét építi fel.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Az a UTC-idő, amely előtt a titkos adatok nem használhatók.
Ha nincs megadva, a titkos attribútum NotBefore attribútumának meglévő értéke változatlan marad.

```yaml
Type: System.Nullable`1[System.DateTime]
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
Ha ez a kapcsoló meg van adva, a Secret objektumot adja vissza.

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

### -Tag
Titkos címkéket képviselő hashtable.
Ha nincs megadva, a titkos kód meglévő címkéi változatlanok maradnak.
Címke eltávolítása üres hashtable megadásával.

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

### -Version
Titkos verzió.
A parancsmag a tároló nevéből, az aktuálisan kijelölt környezetből, a titkos névből és a titkos verzióból építi fel egy titkos név teljes tartománynevét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## KIMENETEK

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
