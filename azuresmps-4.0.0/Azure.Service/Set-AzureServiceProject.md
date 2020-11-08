---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015819"
---
# Set-AzureServiceProject

## Áttekintés
Az aktuális szolgáltatás alapértelmezett helyének, előfizetésének, tárolóhelyének és tárolási fiókjának beállítása.

## SZINTAXISA

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureServiceProject** parancsmag a bevezetési helyet, a bővítőhelyet, a tárolási fiókot és az aktuális szolgáltatás előfizetését állítja be.
Ezek az értékek akkor használhatók, amikor a szolgáltatást közzéteszi a felhőben.

## Példák

### 1. példa: alapvető beállítások
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

A szolgáltatás üzembe helyezési helyének beállítása az észak-közép-amerikai régióban.
Beállítja a telepítő bővítőhelyét a termeléshez. Beállítja azt a tárolási fiókot, amely a myStorageAccount a szolgáltatás meghatározásához fog szolgálni.
Beállítja azt az előfizetést, amely a szolgáltatást a mySubscription-ra fogja üzemeltetni.
Minden alkalommal, amikor a szolgáltatást közzéteszi a felhőben, az az észak-közép-amerikai régióban található adatközpontban fog megjelenni, és a megadott előfizetési és tárolási fiókot fogja használni.

## PARAMÉTEREK

### -Hely
Az a terület, ahol a szolgáltatást üzemeltetni fogják.
Ezt az értéket akkor használja a rendszer, amikor a szolgáltatást közzéteszi a felhőben.
Lehetséges értékek: bárhol Ázsiában, bárhol Európában, bárhol, Kelet-ázsiai, Dél-Közép-amerikai, észak-európai, Dél-Közép-amerikai, Délkelet-ázsiai, Nyugat-európai, Nyugat-amerikai.

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

### -PassThru
Azt jelzi, hogy ez a parancsmag egy olyan objektumot ad eredményül, amely a működéséhez szükséges elemet jelképezi.
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

### -Slot
Az a tárolóhely (termelés vagy megállóhely), amelyben a szolgáltatást üzemeltetni fogják.
Ezt az értéket akkor használja a rendszer, amikor a szolgáltatást közzéteszi a felhőben.
Lehetséges értékek: termelés, megállóhelyek.

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

### -Tárterület
A szervizcsomagnak a felhőbe való feltöltéséhez használandó tárolási fiók.
Ha a tárolási fiók nem létezik, akkor a rendszer akkor hozza létre, amikor a szolgáltatást közzéteszi a felhőben.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI
* Node-dev, php-dev, Python-dev

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureServiceProject](./New-AzureServiceProject.md)

[Közzététel – AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


