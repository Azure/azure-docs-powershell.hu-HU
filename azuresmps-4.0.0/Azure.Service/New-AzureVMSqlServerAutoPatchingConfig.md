---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016191"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Áttekintés
Létrehoz egy konfigurációs objektumot a virtuális gép automatikus javításához.

## SZINTAXISA

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot a virtuális gép automatikus javításához.

## Példák

### Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

Ez a parancs konfigurációs objektumot hoz létre, amellyel beállítható az automatikus javítás a set-AzureVMSqlServerExtension használatával.

## PARAMÉTEREK

### -DayOfWeek
A hét azon napját adja meg, amikor a frissítéseket telepíteni kell.

A paraméter elfogadható értékei a következők:

- Vasárnap
- Hétfő
- Kedd
- Szerda
- Csütörtök
- Péntek
- Szombat
- Mindennapos

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

### – Engedélyezés
Azt jelzi, hogy a virtuális gép automatikus javítás engedélyezve van.
Ha engedélyezi az automatikus javítást, a parancsmag interaktív módba fogja helyezni a Windows Update szolgáltatást.
Ha letiltja az automatikus javítást, a Windows Update beállításai nem változnak.

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

### -MaintenanceWindowDuration
A karbantartás ablak időtartamát adja meg.
Az automatizált javítással elkerülhetők az adott ablakon kívüli virtuális gépek elérhetőségét befolyásoló műveletek.
Csak 30 perc lépés megengedett.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
A karbantartás ablak indításakor megjelenő nap óráját adja meg.
Ez az időpont határozza meg, hogy mikor induljon el a frissítések telepítése, és az órára van kerekítve.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Annak meghatározása, hogy fontos frissítéseket kell-e szerepeltetni.

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

### AutoPatchingSettings
Ez a parancsmag visszaadja az objektumot az automatizált javítások beállításai között.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[Remove-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


