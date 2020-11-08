---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015552"
---
# Get-AzureStorSimpleTask

## Áttekintés
Egy tevékenység állapotát StorSimple eszközön kapja.

## SZINTAXISA

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleTask** parancsmag egy olyan tevékenység állapotát kérdezi le, amely az Azure StorSimple-eszközön aszinkron módon fut.

A StorSimple-eszközök kezelésekor a legtöbb létrehozás, olvasás, frissítés és törlés művelet aszinkron módon futtatható.
A Windows PowerShell egy **TaskId** ad eredményül.
Használja az azonosítót a tevékenység aktuális állapotának a beolvasásához.

## Példák

### Példa 1: tevékenység állapotának beszerzése
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

Ez a parancs a megadott azonosítót tartalmazó tevékenység állapotát kapja meg.
Az eredmények azt mutatják, hogy a tevékenység állapota befejeződött, és a sikeres eredmény eredménye.

## PARAMÉTEREK

### -InstanceId
Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelynek a parancsmagja követi az állapotot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
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

### Nincs

## KIMENETEK

### JobStatusInfo
Ez a parancsmag egy **TaskStatusInfo** -objektumot ad eredményül, amely az alábbi mezőket tartalmazza: 

- **Hiba lép** fel.
**ErrorDetails** , amely **kódot** és **üzenetet** tartalmaz.
- **TaskId**.
**Karakterlánc**.
Annak a tevékenységnek az azonosítója, amelyhez az állapotot visszaadja.
- **TaskSteps**.
**IList \<TaskStep\>**.
Minden **TaskStep** -objektum tartalmaz **részleteket** , **errorcode** , **üzenetet** , **eredményt** és **állapotot**.
- **Result (eredmény** )
**TaskResult** , amely a tevékenység teljes eredményét tartalmazza.
Az érvényes értékek a következők: nem sikerült, sikerült, PartialSuccess, lemondott és érvénytelen.
- **Állapotot**.
**TaskStatus** , amely a tevékenység teljes futási állapotát tartalmazza.
Az érvényes értékek a következők: Inprogress, érvénytelen és befejezett.
- **TaskResult**.
**TaskResult** , az **eredmény** és az **állapot** alapján kiszámított érték.
Az érvényes értékek a következők: sikertelenek, sikeresek, inelőrehaladás, PartialSuccess, lemondás és érvénytelen.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

