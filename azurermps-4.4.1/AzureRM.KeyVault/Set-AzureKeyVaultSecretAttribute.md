---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://go.microsoft.com/fwlink/?LinkId=690305
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: 9d9bd8a14b3a24d6001a7f1c2663b05a1e427f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504099"
---
# Set-AzureKeyVaultSecretAttribute

## Áttekintés
A titkos kulcs attribútumait frissíti a kulcs boltozatában.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureKeyVaultSecretAttribute** parancsmag a titkos kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.

## Példák

### Példa 1: a titok attribútumainak módosítása
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

Az első négy parancs a lejárat, a NotBefore, a címkék és a környezeti típus attribútumait definiálja, valamint az attribútumokat változókban tárolhatja.

A végleges parancs módosította a ContosoVault nevű kulcs boltozatának attribútumait a tárolt változók használatával.

### 2. példa: a címke és a tartalom típusának törlése titoknak
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Ez a parancs a contoso nevű fő boltozatban a titkos nevű HR-verzió megadott verziójához tartozó címkéket és tartalomtípust törli.

### 3. példa: a titok jelenlegi verziójának letiltása, akinek a neve vele kezdődik
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

Az első parancs a contoso karakterlánc értékét a $Vault változóban tárolja.

A második parancs a karakterlánc értékét a $Prefix változóban tárolja.

A harmadik parancs az Get-AzureKeyVaultSecret parancsmagot használja a megadott kulcsfájl titkainak kinyerésére, majd ezeket a titkokat átadja a **Where-Object** parancsmagnak. A **Where-Object** parancsmag kiszűri a karakterrel kezdődő nevek titkát. A parancs bekapcsolja a szűrőhöz igazodó titkot az Set-AzureKeyVaultSecretAttribute parancsmaghoz, amely letiltja őket.

### 4. példa: a ContentType beállítása a titok minden verziójában
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

Az első három parancs a *VaultName* , a *név* és a *ContentType* paraméterben használható karakterlánc-változók definiálását adja meg. A negyedik parancs az Get-AzureKeyVaultKey parancsmagot használja a megadott kulcsok beolvasására, és a kulcsokat a Set-AzureKeyVaultSecretAttribute parancsmagba a tartalomtípusok XML-be való beállításához adja.

## PARAMÉTEREK

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

### -ContentType
A titok tartalomtípusát adja meg. Ha nem adja meg ezt a paramétert, az aktuális titok tartalomtípusa nem változik. Ha el szeretné távolítani a meglévő tartalomtípust, adjon meg egy üres karakterláncot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Engedélyezés
Azt jelzi, hogy engedélyezni kell-e a titkot. A titok engedélyezéséhez $False megadhatja a titkot vagy a $Truet. Ha nem adja meg ezt a paramétert, az aktuális titok engedélyezett vagy letiltott állapota nem változik.

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
Itt adhatja meg azt a dátumot és időpontot, amikor a titok lejár.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A titok nevét adja meg. Ez a parancsmag a titok teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Itt adhatja meg azt a koordinált általános időpontot (UTC), amely előtt a titkos kulcs nem használható.
Ha nem adja meg ezt a paramétert, az aktuális titok NotBefore attribútuma nem változik.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
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

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
A módosítani kívánt fő pince nevét adja meg.
Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és az aktuálisan kiválasztott környezet alapján építi fel.

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

### -Verzió
A titok verziószámát adja meg.
Ez a parancsmag a titkos név, az aktuálisan kijelölt környezet, a titkos név és a titkos verzió alapján építi be a titok teljes tartománynevét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## KIMENETEK

### Microsoft. Azure. Command. kulccsal. modellek. Secret
Visszaadja a Microsoft. Azure. Command. kulccsal. models. Secret objektumot, ha a PassThru meg van adva. Ellenkező esetben semmit sem ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)
