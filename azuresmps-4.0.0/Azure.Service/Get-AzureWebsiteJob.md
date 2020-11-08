---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016273"
---
# Get-AzureWebsiteJob

## Áttekintés
A webhelyhez társított webes feladatok beolvasása.

## SZINTAXISA

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A webhelyhez társított webes feladatok beolvasása.

## Példák

### 1. példa: konkrét webes munkaköri adatok beolvasása
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

A MyWebJob nevű internetes feladatot kapja a MyWebsite Production slotból.

### 2. példa: a webhely összes webes feladatának beszerzése
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

A MyWebsite-termelési bővítőhelyhez társított összes webes feladat beolvasása.

### 3. példa: az összes aktivált webes feladat beszerzése
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

Az összes kezdeményezett webes munkahely beolvasása a MyWebsite átmeneti tárolóhelyéről.

## PARAMÉTEREK

### -Feladatnév
A webes feladat neve

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

### -JobType
A webes feladat típusa.
A paraméter elfogadható értékei a következők:

- Megjelenő
- Folyamatos

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

### -Name (név)
Az Azure-webhely neve.

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
Az Azure-webhely tárolóhelyének neve.

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

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Új – AzureWebsiteJob](./New-AzureWebsiteJob.md)

[Remove-AzureWebsiteJob](./Remove-AzureWebsiteJob.md)

[Start-AzureWebsiteJob](./Start-AzureWebsiteJob.md)

[Stop-AzureWebsiteJob](./Stop-AzureWebsiteJob.md)


