---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015637"
---
# Get-AzureOSVersion

## Áttekintés
Felsorolja az összes Azure Guest operációs rendszert.

## SZINTAXISA

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureOSVersion** parancsmag felsorolja az összes elérhető Azure Guest operációs rendszert.

## Példák

### Példa 1: az összes elérhető operációs rendszer beszerzése
```
PS C:\> Get-AzureOSVersion
```

Ez a parancs olyan objektumot olvas be, amely tartalmazza a vendég operációs rendszerek összes verziójának listáját a jelenlegi előfizetésben.

### 2. példa: az operációs rendszer adatainak megjelenítése táblázatban
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

Ez a parancs olyan objektumot olvas be, amely tartalmazza a vendég operációs rendszerek összes verziójának listáját a jelenlegi előfizetésben.
A parancs a pipeline operátor segítségével átadja őket a **Format-Table** parancsmagnak.
Az adott parancsmag olyan táblázatként formázza őket, amely az operációs rendszer családját, az operációs rendszer családi címkéjét és verzióját jeleníti meg.

## PARAMÉTEREK

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

[Get-AzureOSDisk](./Get-AzureOSDisk.md)


