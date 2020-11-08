---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015850"
---
# Set-AzureStorageAccount

## Áttekintés
Egy Azure-előfizetésben frissíti a tárolási fiók tulajdonságait.

## SZINTAXISA

### AccountType (alapértelmezett)
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GeoReplicationEnabled
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureStorageAccount** parancsmag frissíti az Azure Storage-fiók tulajdonságait az aktuális előfizetésben.
A megadható tulajdonságok: **címke** , **Leírás** , **típus** és **GeoReplicationEnabled**.

## Példák

### Példa 1: a tárolási fiók címkéjének frissítése
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

Ez a parancs frissíti a ContosoStorage01 nevű tárterület-fiók **címke** és **Leírás** tulajdonságát.

### 2. példa: a földrajzi replikálás engedélyezése tárolási fiók esetén
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

Ez a parancs beállítja a **GeoReplicationEnabled** tulajdonságot a ContosoStorage01 nevű tárterület-fiók $false.

### 3. példa: a Geo-replikáció letiltása tárterület-fiók esetén
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

Ez a parancs beállítja a **GeoReplicationEnabled** tulajdonságot a ContosoStorage01 nevű tárterület-fiók $True.

## PARAMÉTEREK

### -Leírás
A tárterület-fiók leírását adja meg.
Lehet, hogy a Leírás legfeljebb 1024 karakter hosszú lehet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoReplicationEnabled
Meghatározza, hogy a tárolási fiók a Geo-replikációs beállítással van-e létrehozva.

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Label (címke)
A tárolási fiók címkéjét adja meg.
Előfordulhat, hogy a címke legfeljebb 100 karakter hosszú lehet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag módosított.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (típus)
A tárolási fiók típusát adja meg.
Az érvényes értékek a következők: 

- Standard_LRS
- Standard_ZRS
- Standard_GRS
- Standard_RAGRS
- Premium_LRS

Ha ez a paraméter nincs megadva, az alapértelmezett érték Standard_GRS.

A *GeoReplicationEnabled* paraméter megadásának hatása megegyezik a *típus* paraméterben Standard_GRS megadásával.

Standard_ZRS vagy Premium_LRS fiókokat nem lehet más típusú fiókokra módosítani, és fordítva.

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

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

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Új – AzureStorageAccount](./New-AzureStorageAccount.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)


