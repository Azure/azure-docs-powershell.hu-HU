---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843910"
---
# Add-AzKeyVaultKey

## Áttekintés
Billentyűt hoz létre a fő tárolóban, vagy egy kulcsot egy fő boltozatba importál.

## SZINTAXISA

### Létrehozás (alapértelmezett)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Importálása
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Add-AzKeyVaultKey** parancsmag egy billentyűt hoz létre az Azure Key Vault-ban, vagy egy kulcsot importál egy fő boltozatba.
Ezzel a parancsmaggal a következő módszerekkel adhat hozzá kulcsokat:

- Hozzon létre egy kulcsot egy hardveres biztonsági modulban (HSM) a Key Vault szolgáltatásban.
- Kulcsot hozhat létre a szoftverben a Key Vault szolgáltatásban.
- Importáljon egy kulcsot a saját hardver biztonsági modulból (HSM) a HSM a Key Vault szolgáltatásba.
- Importáljon egy kulcsot egy. pfx fájlból a számítógépre.
- Importáljon egy kulcsot egy. pfx fájlból a számítógépen a hardver biztonsági moduljaihoz (HSM) a Key Vault szolgáltatásban.

A fenti műveletek bármelyikével alapvető attribútumokat adhat meg, illetve elfogadhat alapértelmezett beállításokat.

Ha olyan billentyűt hoz létre vagy importál, amelynek a neve megegyezik egy meglévő kulccsal, az eredeti kulcs frissül az új kulcshoz megadott értékekkel. A korábbi értékeket a kulcs adott verziójához tartozó, a verziószámot tartalmazó URI-azonosító használatával érheti el. A főbb verziókkal és az URI-struktúrájával kapcsolatos tudnivalók a [kulcsok andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) a Key Vault REST API-ban című dokumentumban olvashatók.

Megjegyzés: Ha egy kulcsot saját hardveres biztonsági modulból szeretne importálni, először létre kell hoznia egy BYOK-csomagot (. BYOK fájlnév-kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészlet használatával. További információt a [HSM-Protected kulcsok létrehozása és továbbítása az Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252)-ban című témakörben találhat.

Ajánlott eljárásként készítsen biztonsági másolatot a kulcsról, miután létrehozta vagy frissíti őket a Backup-AzKeyVaultKey parancsmag használatával. Nincs eltávolítási funkció, ezért ha véletlenül törli a billentyűt vagy törli, majd meggondolja magát, a kulcs nem állítható helyre, hacsak nem rendelkezik biztonsági másolattal.

## Példák

### Példa 1: kulcs létrehozása
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

Ez a parancs létrehoz egy ITSoftware nevű, a contoso nevű kulcsfájl nevű kulccsal védett kulcsot.

### 2. példa: HSM-védelemmel ellátott kulcs létrehozása
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

Ez a parancs egy HSM-védelemmel ellátott billentyűt hoz létre a contoso nevű kulcs boltozatához.

### 3. példa: kulcs létrehozása nem alapértelmezett értékekkel
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

Az első parancs a $KeyOperations változóban tárolja az értékeket dekódolja és ellenőrzi.

A második parancs létrehoz egy **datetime** típusú objektumot, amelyet az UTC a **Get-Date** parancsmag használatával definiál.
Ez az objektum két év múlva adja meg a jövőbeli időpontot. A parancs a $Expires változóban tárolja a dátumot. További információért írja be a következőt: `Get-Help Get-Date` .

A harmadik parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával. Az objektum a jelenlegi UTC időpontot adja meg. A parancs a $NotBefore változóban tárolja a dátumot.

A végleges parancs létrehoz egy ITHsmNonDefault, amely egy HSM-védelemmel ellátott kulcs. A parancs a $KeyOperations tárolt, engedélyezett műveletek értékeit adja meg. A parancs az előző parancsokban létrehozott *lejáratok* és *NotBefore* paramétereinek időpontját adja meg, valamint a nagy SÚLYOSSÁGú és az IT-címkéket. Az új kulcs le van tiltva. A **set-AzKeyVaultKey** parancsmag használatával engedélyezheti azt.

### Példa 4: HSM-védelemmel ellátott kulcs importálása
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

Ez a parancs a ITByok nevű kulcsot a *KeyFilePath* paraméter által megadott helyről importálja. Az importált kulcs egy HSM-védelemmel ellátott kulcs.

Ha egy kulcsot saját hardveres biztonsági modulból szeretne importálni, először létre kell hoznia egy BYOK-csomagot (. BYOK fájlnév-kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészlet használatával.
További információt a [HSM-Protected kulcsok létrehozása és továbbítása az Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252)-ban című témakörben találhat.

### Példa 5: szoftverrel védett kulcs importálása
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Password változóban tárolja. További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .

A második parancs a contoso Key Vault-ban hozza létre a szoftverhez tartozó jelszót. A parancs a $Passwordban tárolt kulcs és jelszó helyét adja meg.

### 6. példa: kulcs importálása és attribútumok hozzárendelése
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Password változóban tárolja.

A második parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával, majd az objektumot az $Expires változóban tárolja.

A harmadik parancs a $tags változót hozza létre a nagy súlyosságú és a címkék beállításához.

A végleges parancs a megadott helyről importálja a kulcsot a HSM-kulcsként. A parancs a $Password tárolt $Expires és jelszóban tárolt elévülési időt adja meg, és a $tagsban tárolt címkéket alkalmazza.

## PARAMÉTEREK

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

### -Destination (cél)
Itt adhatja meg, hogy a kulcsot szoftverrel védett kulcsként vagy HSM-védelemmel ellátott kulccsal szeretné-e hozzáadni a Key Vault szolgáltatásban.
Érvényes értékek: HSM és szoftver.

Megjegyzés: Ha a HSM-t célként szeretné használni, rendelkeznie kell a HSM támogató fő tárolóval. Az Azure Key Vault szolgáltatás szintjeiről és képességeiről további információt az [Azure Key Vault árképzési webhelyén](http://go.microsoft.com/fwlink/?linkid=512521)találhat.

Ezt a paramétert új kulcs létrehozásakor kell megadni. Ha a *KeyFilePath* paraméterrel importál egy billentyűt, akkor ez a paraméter nem kötelező:

- Ha nem adja meg ezt a paramétert, és ez a parancsmag olyan kulcsot importál, amely. byok fájlnév-kiterjesztéssel rendelkezik, a kulcsot HSM-védelemmel ellátott kulcsként importálja. A parancsmag nem tudja importálni a kulcsot szoftveres védelemmel ellátott kulcsként.

- Ha nem adja meg ezt a paramétert, és ez a parancsmag a. pfx fájlnév-kiterjesztésű kulcsot importálja, az a kulcsot szoftveres védelemmel ellátott kulcsként importálja.

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Letiltása
Azt jelzi, hogy a felvenni kívánt kulcs a letiltott állapotú eredeti állapotra van állítva. A billentyű használatát minden próbálkozás sikertelen lesz. Akkor használja ezt a paramétert, ha előre betöltődik a később engedélyezni kívánt billentyűk.

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

### -Lejár
A lejárati idő **datetime** objektumként való megadása a parancsmag által hozzáadott kulcshoz. Ez a paraméter koordinált univerzális időpontot (UTC) használ. Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot. További információért írja be a következőt: `Get-Help Get-Date` . Ha nem adja meg ezt a paramétert, a kulcs nem jár le.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyFilePassword
Az importált fájlhoz tartozó jelszót **SecureString** -objektumként adja meg. **SecureString** objektum beolvasásához használja a **ConvertTo-SecureString** parancsmagot. További információért írja be a következőt: `Get-Help ConvertTo-SecureString` . A. pfx fájlnév-kiterjesztésű fájlok importálásához meg kell adnia ezt a jelszót.

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
A parancsmag által importált fontos anyagot tartalmazó helyi fájl elérési útját adja meg.
Az érvényes fájlnév-kiterjesztések. byok és. pfx.

- Ha a fájl. byok fájl, az importálás után a rendszer automatikusan védi a kulcsot, és nem tudja felülírni ezt az alapértelmezett HSM.

- Ha a fájl. pfx fájl, a kulcs automatikusan védett a szoftverrel az importálás után. Az alapértelmezett beállítás felülbírálásához állítsa a *cél* paramétert a HSM értékre, hogy a kulcs HSM-védelemmel legyen ellátva.

Ha ezt a paramétert adja meg, a *cél* paraméter nem kötelező.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Megadja azokat a műveleteket, amelyeket a parancsmag által hozzáadott kulccsal végezhet el.
Ha nem adja meg ezt a paramétert, akkor az összes művelet elvégezhető.

A paraméter elfogadható értékei: a [JSON-webkulcs (JWK) specifikációja](http://go.microsoft.com/fwlink/?LinkID=613300)által meghatározott főbb műveletek vesszővel elválasztott listája:

- Beavatkozik
- Visszafejtése
- Wrap
- Tördelésének megszüntetéséhez
- Jel
- Ellenőrizze

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak a kulcsnak a nevét adja meg, amelyet fel szeretne venni a kulcs boltozatához. Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján. A névnek 0-9 csak az 1-es, a-z, A-z és A-(a kötőjel szimbólumot) tartalmazó 63-karakterből kell állnia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Itt adhatja meg az időt **datetime** objektumként, amely előtt a kulcs nem használható. Ez a paraméter az UTC-t használja. Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot. Ha nem adja meg ezt a paramétert, akkor a billentyű azonnal használható.

```yaml
Type: DateTime
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
Annak a kulcsnak a nevét adja meg, amelyre a parancsmag hozzáadja a kulcsot. Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.

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

### Microsoft. Azure. Command. Vault. models. Bundle

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
