---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505163"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Áttekintés
Létrehoz egy konfigurációs objektumot egy virtuális gépen történő automatikus javításhoz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureVMSqlServerAutoPatchingConfig** parancsmag létrehoz egy konfigurációs objektumot egy virtuális gépen az automatikus javításhoz.

## Példák

### Példa 1: konfigurációs objektum létrehozása az automatikus javítás konfigurálásához
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
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
Ezt a konfigurációs elemet más parancsmagok, például az Set-AzureRmVMSqlServerExtension parancsmag esetében is megadhatja.

## PARAMÉTEREK

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

### -PatchCategory
Annak meghatározása, hogy fontos frissítéseket kell-e szerepeltetni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
@ {Text =}

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@ {Text =}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

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

[Új – AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


