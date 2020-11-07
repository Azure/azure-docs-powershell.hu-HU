---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845729"
---
# New-AzVMSqlServerAutoPatchingConfig

## Áttekintés
Létrehoz egy konfigurációs objektumot egy virtuális gépen történő automatikus javításhoz.

## SZINTAXISA

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## Leírás
A **New-AzVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot egy virtuális gépen az automatikus javításhoz.

## Példák

### Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Ez a parancs konfigurációs objektumot hoz létre a javításhoz.
A parancs a hét napját adja meg, és meghatározza a karbantartási ablakot.
Ez a beállítás lehetővé teszi az ezeket az értékeket használó javítások javítását.
A parancs az eredményt a $AutoBackupConfig változóban tárolja.
Ezt a konfigurációs elemet más parancsmagok, például az Set-AzVMSqlServerExtension parancsmag esetében is megadhatja.

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
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Engedélyezés
Azt jelzi, hogy a virtuális gép automatikus javítás engedélyezve van.
Ha engedélyezi az automatikus javítást, a parancsmag a Windows Update funkciót interaktív módba teszi.
Ha letiltja az automatikus javítást, a Windows Update beállításai nem változnak.

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

### -MaintenanceWindowDuration
A karbantartási ablak időtartamát adja meg percben.
Az automatizált javítás elkerüli az ablakon kívüli virtuális gépek elérhetőségét érintő műveletek végrehajtását.
30 perc többszörösét adja meg.

```yaml
Type: System.Int32
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
Ez az időpont határozza meg, hogy mikor induljon el a frissítések telepítése.

```yaml
Type: System.Int32
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
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. AutoPatchingSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


