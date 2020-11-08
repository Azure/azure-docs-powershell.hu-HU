---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016031"
---
# Start-AzureEmulator

## Áttekintés
Elindítja a számítási és a tárolási emulátort.

## SZINTAXISA

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Start-AzureEmulator** parancsmag mind a számítási, mind a tároló emulátorral elindul, és az aktuális szolgáltatást a számítási emulátorban tárolja.

## Példák

### 1. példa: az emulátor elindítása és a böngésző elindítása
```
PS C:\> Start-AzureEmulator -L
```

Ez a példa futtatja a szolgáltatást az Azure emulátorban, és egy új böngészőablakot indít az emulált szolgáltatásban.

## PARAMÉTEREK

### -Launch (indítás)
Az emulátorban való üzemeltetés után megnyílik egy új böngészőablak a szolgáltatásban.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Üzemmód
Az emulátor üzemmódot adja meg.
Az érvényes értékek: teljes és expressz.
Az alapértelmezett érték az Express.

```yaml
Type: ComputeEmulatorMode
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureServiceProject](./New-AzureServiceProject.md)

[Közzététel – AzureServiceProject](./Publish-AzureServiceProject.md)

[Stop-AzureEmulator](./Stop-AzureEmulator.md)


