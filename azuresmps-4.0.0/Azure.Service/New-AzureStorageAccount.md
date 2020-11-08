---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016204"
---
# New-AzureStorageAccount

## Áttekintés
Új tárolási fiókot hoz létre Azure-előfizetésben.

## SZINTAXISA

### ParameterSetAffinityGroup (alapértelmezett)
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### ParameterSetLocation
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageAccount** parancsmag létrehoz egy fiókot, amely hozzáférést biztosít az Azure Storage Services szolgáltatáshoz.
A tárterület-fiók globálisan egyedi erőforrás a tárolási rendszeren belül.
A fiók a blob-, a várólista-és a táblázat-szolgáltatások fölérendelt névtere.

## Példák

### Példa 1: a megadott affinitási csoport tárolási fiókjának létrehozása
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

Ez a parancs létrehoz egy tárolási fiókot a megadott affinitási csoporthoz.

### 2. példa: tárterület-fiók létrehozása megadott helyen
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

A parancs létrehoz egy tárterület-fiókot a megadott helyen.

## PARAMÉTEREK

### -AffinityGroup
Egy meglévő affinitási csoport nevét adja meg az aktuális előfizetésben.
Megadhatja a *helyet* vagy a *AffinityGroup* paramétert is, de mindkettőt nem.

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Leírás
A tárterület-fiók leírását adja meg.
A Leírás legfeljebb 1024 karakter hosszú lehet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Előfordulhat, hogy a címke hossza legfeljebb 100 karakter lehet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Az Azure Data Center helyét adja meg, ahol a tárolási fiók létrejön.
A *helyet* vagy a *AffinityGroup* paramétert is megadhatja, de mindkettőt nem.

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
A tárterület-fiók nevét adja meg.
A tárolási fiók nevének egyedinek kell lennie az Azure-ban, és a hosszúság 3 és 24 karakter közé kell lennie, és csak kis betűket és számokat kell használnia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

Standard_ZRS vagy Premium_LRS fiókokat nem lehet más típusú fiókokra módosítani, és fordítva.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


