---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: d2c153cf0ae2f5cffbf47656d3ae64a531cb780b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413795"
---
# Add-AzKeyVaultKey

## SYNOPSIS
Kulcsot hoz létre egy kulcstárban, vagy kulcsot importál egy kulcstárba.

## SZINTAXIS

### InteractiveCreate (alapértelmezett)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzKeyVaultKey** parancsmag létrehoz egy kulcsot egy kulcstárban az Azure Kulcstárban, vagy importál egy kulcsot egy kulcstárba.
Ezzel a parancsmagkal az alábbi módszerek bármelyikével adhat hozzá billentyűket:
- Hozzon létre egy kulcsot egy hardverbiztonsági modulban (HSM) a kulcstár szolgáltatásban.
- Termékkulcs létrehozása a kulcstár szolgáltatásban.
- Importálhat egy kulcsot a saját hardveres biztonsági modulból (HSM) a kulcstár szolgáltatásban található HSM-ekbe.
- Importálja a kulcsot egy .pfx fájlból a számítógépen.
- A kulcstár szolgáltatásban egy .pfx fájlból hardveres biztonsági modulokba (HSM-eket) importálhat.
E műveletek bármelyikéhez meg kell adnia a legfontosabb attribútumokat, vagy el kell fogadnia az alapértelmezett beállításokat.
Ha olyan kulcsot hoz létre vagy importál, amely neve megegyezik a kulcstárban meglévő kulcs nevével, az eredeti kulcs frissül az új kulcshoz megadott értékekkel. A korábbi értékeket a kulcs adott verziójához használt verzióspecifikus URI azonosítóval tudja elérni. A legfontosabb verziókról és az URI-struktúráról a Kulcstár REST API dokumentációjában található A kulcsok és a titkos információk szolgáltatásról olvashat. [](http://go.microsoft.com/fwlink/?linkid=518560)
Megjegyzés: Ha saját hardveres biztonsági modulból importálni kívánt kulcsot, először létre kell hoznia egy BYOK-csomagot (egy .byok kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészletével. További információt az Azure-kulcstárhoz HSM-Protected kulcsok létrehozása és [átvitele.](http://go.microsoft.com/fwlink/?LinkId=522252)
Gyakorlati megoldásként a termékkulcsról a létrehozása vagy frissítése után is biztonsági Backup-AzKeyVaultKey parancsmag használatával. Nincs előtűnés funkció, ezért ha véletlenül törli vagy törli a kulcsot, majd meggondolja magát, a kulcs csak akkor állítható helyre, ha biztonsági másolatot készít róla.

## PÉLDÁK

### 1. példa: Kulcs létrehozása
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Ez a parancs létrehoz egy ITSoftware nevű szoftver védett kulcsot a Contoso nevű kulcstárban.

### 2. példa: HSM-védelemű kulcs létrehozása
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Ez a parancs létrehoz egy HSM által védett kulcsot a Contoso nevű kulcstárban.

### 3. példa: Nem alapértelmezett értékeket tartalmazó kulcs létrehozása
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Az első parancs az értékeket visszafejti és ellenőrzi a $KeyOperations változóban.
A második parancs a **Get-Date** parancsmag használatával létrehozza az **UTC-ben** definiált DateTime objektumot.
Ez az objektum a jövőben két évet ad meg. A parancs ezt a dátumot a $Expires tárolja. További információért írja be a `Get-Help Get-Date` .
A harmadik parancs a **Get-Date** parancsmag használatával hoz létre **DateTime-objektumot.** Ez az objektum az aktuális UTC-időt adja meg. A parancs ezt a dátumot a $NotBefore tárolja.
Az utolsó parancs létrehoz egy ITHsmNonDefault nevű kulcsot, amely egy HSM-védelem alatt áll. A parancs az engedélyezett kulcsműveleteket a $KeyOperations. A parancs az előző  parancsokban létrehozott Lejárati és *NemBefore* paraméterek, valamint a magas súlyosság és az IT címkéit adja meg. Az új kulcs le van tiltva. A beállítás engedélyezéséhez használja a **Set-AzKeyVaultKey** parancsmagot.

### 4. példa: HSM-védelemű kulcs importálása
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Ez a parancs a *KeyFilePath* paraméter által megadott helyről importálja az ITByok nevű kulcsot. Az importált kulcs egy HSM-védelem alatt áll.
Ha saját hardveres biztonsági modulból importálni kívánt kulcsot, először létre kell hoznia egy BYOK-csomagot (egy .byok kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészletével.
További információt az Azure-kulcstárhoz HSM-Protected kulcsok létrehozása és [átvitele.](http://go.microsoft.com/fwlink/?LinkId=522252)

### 5. példa: Szoftver által védett kulcs importálása
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Password tárolja. További információért írja be a `Get-Help
ConvertTo-SecureString` .
A második parancs létrehoz egy szoftverjelszót a Contoso kulcstárban. A parancs a kulcs és a jelszó helyét adja meg a $Password.

### 6. példa: Kulcs importálása és attribútumok hozzárendelése
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Password tárolja.
A második parancs a **Get-Date** parancsmag használatával **dateTime** objektumot hoz létre, majd az objektumot a $Expires tárolja.
A harmadik parancs létrehozza a $tags változót a nagy súlyosságú és az it-it-címkék beállítására.
A végleges parancs egy kulcsot HSM-kulcsként importál a megadott helyről. A parancs megadja a $Expires és a $Password-ban tárolt jelszóban tárolt lejárati időt, és alkalmazza a $tags.

### 7. példa: Kulcs exchange-kulcs (KEK) létrehozása a "hozza el a saját kulcsát" (BYOK) funkcióhoz

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Létrehoz egy kulcsot (más néven kulcs exchange-kulcsot ).</b0> A KEK-nek olyan RSA-HSM kulcsnak kell lennie, amely csak az importálási kulcsművelettel rendelkezik. Csak a kulcstár prémium termékváltozata támogatja az RSA-HSM kulcsokat.
További részletekért lásd: https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

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

### -Destination
Megadja, hogy a kulcs hozzáadva legyen-e szoftveres vagy HSM által védett kulcsként a kulcstár szolgáltatásban.
Érvényes értékek: HSM és Software.
Megjegyzés: Ahhoz, hogy a HSM-et használni tudja célként, olyan kulcstárat kell használnia, amely támogatja a HSM-eket. Az Azure Key Vault szolgáltatásszintjéről és funkcióiról az [Azure Key Vault árazási](http://go.microsoft.com/fwlink/?linkid=512521)webhelyén talál további információt.
Új kulcs létrehozásakor ez a paraméter szükséges. Ha a *KeyFilePath* paraméterrel importál egy kulcsot, a paraméter megadása nem kötelező:
- Ha nem adja meg ezt a paramétert, és ez a parancsmag egy .byok fájlnévkiterjesztésű kulcsot importál, akkor a kulcsot HSM-védelem alatt lévő kulcsként importálja. A parancsmag nem tudja importálni a kulcsot szoftver által védett kulcsként.
- Ha nem adja meg ezt a paramétert, és ez a parancsmag egy .pfx fájlnévkiterjesztésű kulcsot importál, a kulcsot szoftver által védett kulcsként importálja.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Azt jelzi, hogy a hozzáadott kulcs a letiltás kezdeti állapotára van állítva. A kulcs használatára tett minden kísérlet sikertelen lesz. Akkor használja ezt a paramétert, ha előre betölti a később engedélyezni kívánt kulcsokat.

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

### -Lejár
A parancsmag által adott kulcs **Lejárati** idejét adja meg DateTime-objektumként. Ez a paraméter egyezményes világidőt (UTC) használ. **DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot. További információért írja be a `Get-Help Get-Date` . Ha nem adja meg ezt a paramétert, a kulcs nem jár le.

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
Tárolóobjektum.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Az importált fájl jelszavát adja meg **SecureString objektumként.** A **SecureString objektum** beszerzéséhez használja a **ConvertTo-SecureString** parancsmagot. További információért írja be a `Get-Help ConvertTo-SecureString` . A .pfx kiterjesztésű fájlok importálásához meg kell adnia ezt a jelszót.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Egy olyan helyi fájl elérési útját adja meg, amely a parancsmag által importálni kívánt legfontosabb anyagot tartalmazza.
Az érvényes fájlnévkiterjesztések a .byok és a .pfx.
- Ha a fájl .byok fájl, a kulcs az importálás után automatikusan az HSM-ekkel lesz védve, és ez az alapértelmezett beállítás nem bírálható felül.
- Ha a fájl .pfx fájl, a kulcsot az importálás után automatikusan szoftver védi. Az alapértelmezett beállítás felülbírálása érdekében állítsa a Cél paramétert HSM-nek, hogy a kulcs HSM-védelem alatt ússa meg. 
Ha megadja ezt a paramétert, a *Cél* paraméter megadása nem kötelező.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
A parancsmag által hozzáadható billentyűvel elvégezhető műveletek tömbje.
Ha nem adja meg ezt a paramétert, az összes művelet elvégezhető.
A paraméter elfogadható értékei a [JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300)specifikációban meghatározott kulcsműveletek vesszővel elválasztott listája:
- titkosítás
- visszafejtése
- wrapKey
- unwrapKey
- aláírás
- ellenőrzés
- importálás (csak kEK esetén lásd a 7. példát)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A kulcstárhoz hozzáadni megfelelő kulcs neve. Ez a parancsmag egy kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstár neve és az aktuális környezet alapján. A névnek egy 1 és 63 karakter hosszúságú karakterláncnak kell lennie, amely csak 0-9, a-z, A-Z és - (kötőjelet) tartalmaz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Azt az időt adja meg **DateTime-objektumként,** amely előtt a kulcs nem használható. Ez a paraméter az UTC-t használja. **DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot. Ha nem adja meg ezt a paramétert, a kulcs azonnal használható.

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

### -ResourceId
Tároló erőforrásazonosítója.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
RSA-billentyű mérete bitben. Ha nincs megadva, a szolgáltatás biztonságos alapértelmezett beállítást biztosít.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
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

### -VaultName
Annak a kulcstárnak a nevét adja meg, amelyhez ez a parancsmag hozzáadja a kulcsot. Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

