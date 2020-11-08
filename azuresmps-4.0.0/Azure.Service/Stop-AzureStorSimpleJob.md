---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016012"
---
# Stop-AzureStorSimpleJob

## Áttekintés
Leállít egy StorSimple-feladatot.

## SZINTAXISA

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **stop-AzureStorSimpleJob** parancsmag egy folyamatban lévő StorSimple-feladatot leáll.
A munkafolyamatokat a példány-AZONOSÍTÓk vagy a feladatnév megadásával is megadhatja.

## Példák

### 1. példa: a feladatok leállítása egy eszközön
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

Ez a parancs a **Get-AzureStorSimpleJob** parancsmag használatával kapja meg a Device07 nevű eszköz munkahelyeit.
A parancs a pipeline operátorral továbbítja a feladatokat az aktuális parancsmaghoz.
Az aktuális parancsmag megszünteti azokat a feladatokat, amelyekre a parancs a parancsot átadja.
A parancs az *erő* paramétert adja meg, ezért a feladat leállítása előtt nem kér megerősítést.

### 2. példa: adott feladat leállítása
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

Ez a parancs leállítja a megadott példány-azonosítót tartalmazó munkát.

## PARAMÉTEREK

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -InstanceId
A leállításhoz adja meg az eszköz feladatának AZONOSÍTÓját.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Egy Azure-profilt ad meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### DeviceJobDetails
Ez a parancsmag azokat a **DeviceJob** részletezi, amelyekre a parancsmag leáll.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


