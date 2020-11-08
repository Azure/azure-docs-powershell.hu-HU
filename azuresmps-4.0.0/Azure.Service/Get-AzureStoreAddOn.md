---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015547"
---
# Get-AzureStoreAddOn

## Áttekintés
Az elérhető Azure Store bővítmények beolvasása

## SZINTAXISA

### ListAvailable
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetAddOn
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A rendelkezésre álló bővítmények beszerzése az Azure Store áruházból, vagy az aktuális előfizetéshez tartozó meglévő bővítmény-példányok beszerzése.

## Példák

### Példa 1
```
PS C:\> Get-AzureStoreAddOn
```

Ez a példa beolvassa a jelenlegi előfizetés összes megvásárolt bővítmény-példányát.

### 2. példa
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

Ez a példa az Amerikai Egyesült Államokban az Azure Store áruházból beszerezhető összes bővítményt megkapja.

### 3. példa
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

Ez a példa egy MyAddOn nevű bővítményt kap a jelenlegi előfizetéshez tartozó megvásárolt bővítményről.

## PARAMÉTEREK

### -Ország
Ha meg van adva, akkor csak a megadott országban elérhető Azure Store bővítmény-példányokat adja vissza.
Az alapértelmezett érték az "amerikai".

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ListAvailable
Ha meg van adva, elérhetővé válik az Azure áruházból beszerezhető bővítmények.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A megadott nevű bővítményt adja vissza.

```yaml
Type: String
Parameter Sets: GetAddOn
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStoreAddOn](./New-AzureStoreAddOn.md)

[Remove-AzureStoreAddOn](./Remove-AzureStoreAddOn.md)

[Set-AzureStoreAddOn](./Set-AzureStoreAddOn.md)


