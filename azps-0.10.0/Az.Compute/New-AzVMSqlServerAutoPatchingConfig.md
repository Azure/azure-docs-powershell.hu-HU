---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398257"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
Konfigurációs objektumot hoz létre automatikus javításhoz egy virtuális gépen.

## SZINTAXIS

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot az automatikus javításhoz egy virtuális gépen.

## PÉLDÁK

### 1. példa: Az automatikus javítás konfigurálása konfigurációs objektum létrehozása
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Ez a parancs konfigurációs objektumot hoz létre javításra.
A parancs megadja a hét napját és a karbantartási ablakot.
Ez a konfiguráció lehetővé teszi az ezeket az értékeket használó javításokat.
A parancs az eredményt a $AutoBackupConfig tárolja.
Ezt a konfigurációs elemet más parancsmagok, például a Set-AzVMSqlServerExtension is megadhatja.

## PARAMETERS

### -DayOfWeek
A hétnek azt a napját adja meg, amikor frissítéseket kell telepíteni.

A paraméter elfogadható értékei a következőek:

- vasárnap
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
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Azt jelzi, hogy a virtuális géphez engedélyezve van az automatikus javítás.
Ha engedélyezi a parancsmag automatikus javítását, a Windows Update interaktív üzemmódba vált.
Ha letiltja az automatikus javításokat, a Windows Update beállításai nem változnak.

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

### -MaintenanceWindowDuration
A karbantartási ablak időtartamát adja meg percben.
Az automatikus javításokkal elkerülhetők olyan műveletek, amelyek hatással lehetnek a virtuális gépek ezen az ablakon kívüli elérhetőségére.
Adja meg a 30 perc többszörösét.

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
A karbantartási ablak indításakor a nap óráját adja meg.
Ez az idő azt határozza meg, hogy mikor indulnak el a frissítések.

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
Megadja, hogy a fontos frissítéseket is meg kell-e kapni.

```yaml
Type: String
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs
Ez a parancsmag semmilyen bemenetet nem fogad el.

## KIMENETEK

### AutoPatchingSettings
Ez a parancsmag az automatikus javítás beállításait tartalmazza.

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


