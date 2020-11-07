---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
ms.openlocfilehash: df861a5efa87126b5eac1657a2b33b6fbae2110b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843850"
---
# Set-AzKeyVaultKeyAttribute

## Áttekintés
Frissíti a kulcsok attribútumait egy kulcs boltozatában.

## SZINTAXISA

```
Set-AzKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzKeyVaultKeyAttribute** parancsmag a kulcsok szerkeszthető attribútumait frissíti a kulcs boltozatakor.

## Példák

### 1. példa: kulcs módosítása az engedélyezéshez, és a lejárat dátuma és a címkék beállítása
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

Az első parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával. Ez az objektum két év múlva adja meg a jövőbeli időpontot. A parancs a $Expires változóban tárolja a dátumot.
További információért írja be a következőt: `Get-Help Get-Date` .

A második parancs létrehoz egy változót, amely a nagy súlyosságú és a számviteli adatok címkézését tárolja.

A végleges parancs módosítja a ITSoftware nevű kulcsot. A parancs engedélyezi a kulcsot, a lejárati időt az $Expires tárolt időpontra állítja be, és beállítja a $Tags tárolt címkéket.

### 2. példa: kulcs módosítása az összes címke törléséhez
```
PS C:\>Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

Ez a parancs törli az összes címkét a ITSoftware nevű kulcs adott verziójához.

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

### – Engedélyezés
Itt adhatja meg, hogy engedélyezi vagy letiltja-e a billentyűt. A $True értéke lehetővé teszi a kulcs használatát. A $False értéke letiltja a billentyűt. Ha nem adja meg ezt a paramétert, ez a parancsmag nem módosítja a kulcs állapotát.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lejár
A lejárati idő **datetime** objektumként való megadása a parancsmag által frissített kulcshoz. Ez a paraméter koordinált univerzális időpontot (UTC) használ. Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot. További információért írja be a következőt: `Get-Help Get-Date` .

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

### -KeyOps
Megadja azokat a műveleteket, amelyeket a parancsmag által hozzáadott kulccsal végezhet el.
Ha nem adja meg ezt a paramétert, akkor az összes művelet elvégezhető.

A paraméter elfogadható értékei a JSON webkulcs specifikációja által meghatározott főbb műveletek vesszővel elválasztott listája. Ezek az értékek (kis-és nagybetűk):

- beavatkozik
- visszafejtése
- wrap
- tördelésének megszüntetéséhez
- jel
- Ellenőrizze
- hát
- visszaállítása

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
A frissítendő kulcs nevét adja meg. Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Itt adhatja meg az időt **datetime** objektumként, amely előtt a kulcs nem használható.
Ez a paraméter az UTC-t használja.
Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.

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

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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
Annak a kulcsnak a nevét adja meg, amelyben ez a parancsmag módosítja a kulcsot.
Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.

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

### -Verzió
A kulcs verziószámát adja meg.
Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
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

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)
