---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016309"
---
# Get-AzureService

## Áttekintés
Egy olyan objektumot ad eredményül, amely információkat nyújt az aktuális előfizetéshez tartozó felhőalapú szolgáltatásokról.

## SZINTAXISA

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureService** parancsmag olyan lista-objektumot ad eredményül, amely az aktuális előfizetéshez társított összes Azure Cloud-szolgáltatással rendelkezik.
Ha a *szolgáltatásnév* paramétert adja meg, a **Get-AzureService** csak a megfelelő szolgáltatás adatait adja eredményül.

## Példák

### 1. példa: információk kérése az összes szolgáltatásról
```
PS C:\> Get-AzureService
```

Ez a parancs olyan objektumot ad eredményül, amely információkat tartalmaz az aktuális előfizetéshez társított összes Azure-szolgáltatásról.

### 2. példa: információ kérése adott szolgáltatásról
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

Ez a parancs információt ad az $MySvc szolgáltatásról.

### 3. példa: elérhető metódusok és tulajdonságok megjelenítése
```
PS C:\> Get-AzureService | Get-Member
```

Ez a parancs a **Get-AzureService** parancsmagban elérhető tulajdonságokat és metódusokat jeleníti meg.

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

### -Szolgáltatásnév
Annak a szolgáltatásnak a nevét adja meg, amelyből adatokat szeretne visszaadni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### HostedServiceContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


