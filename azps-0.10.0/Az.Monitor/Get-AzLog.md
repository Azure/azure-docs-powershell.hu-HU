---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: f6000574313942c774c9243d9a4d4a42caa28820
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842041"
---
# Get-AzLog

## Áttekintés
Tevékenység-naplózási események beolvasása

## SZINTAXISA

### GetByCorrelationId
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceId
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzLog** parancsmag tevékenység-naplózási eseményeket keres.
Az események az aktuális előfizetési AZONOSÍTÓval, korrelációs AZONOSÍTÓval, erőforrás csoporttal, erőforrás-AZONOSÍTÓval vagy erőforrás-szolgáltatóval kapcsolhatók be.

## Példák

### Példa 1: esemény naplójának beszerzése előfizetés-AZONOSÍTÓval
```
PS C:\>Get-AzLog
```

Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, az aktuális dátumtól/időponttól számított 7 napot tartalmazó legtöbb 1000-eseményben szerepel.

### 2. példa: az esemény naplójának beszerzése előfizetés-AZONOSÍTÓval maximális számú eseménnyel
```
PS C:\>Get-AzLog -MaxRecord 100
```

Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, az aktuális dátumtól/időponttól számított 7 napot tartalmazó legtöbb 100-eseményben szerepel.

### 3. példa: az előfizetési AZONOSÍTÓval beolvashatja az eseménynaplót kezdési időponttal.
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

Ez a parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, a 2017-06-01T10:30 helyi időpontra, illetve az aktuális dátumtól/időponttól számított 30 napnál nem régebbi 90 verzió esetén jeleníti meg a legtöbb 1000-eseményt.

### Példa 4: az esemény naplójának beszerzése előfizetéses AZONOSÍTÓval a kezdési és befejezési időponttal.
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Ez a 1000 parancs a felhasználó előfizetési AZONOSÍTÓJÁHOZ tartozó, a 2017-04-01T10:30 helyi idő, illetve 2017-04-14T11:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz a megtartási időszakból.

### Példa 5: esemény naplójának beszerzése korrelációs AZONOSÍTÓval
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 1000-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot. 
**Megjegyzés** : ez általában csak egy esemény.

### 6. példa: a korrelációs AZONOSÍTÓval beolvashatja az eseménynaplót az események maximális számával.
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 100-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot. 
**Megjegyzés** : ez általában csak egy esemény.

### 7. példa: események naplózása a korrelációs AZONOSÍTÓval és a kezdési időponttal
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Ez a parancs a 1000-es számú, a 2017-05-22T04:30:00 helyi idő alatt vagy azt követően a megadott korrelációs AZONOSÍTÓval társított legtöbb-eseményen szerepel, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.
**Megjegyzés** : ez általában csak egy esemény.

### 8. példa: esemény naplójának beszerzése korrelációs AZONOSÍTÓval a kezdési és befejezési időponttal
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Ez a parancs a megadott korrelációs AZONOSÍTÓval társított legtöbb 1000-eseményen (2017-04-15T04:30 helyi időpontban) vagy a 2017-04-25T12:30 helyi idő alatt, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: a retenciós időszak.

### Példa 9: erőforrás-csoport eseménynaplójának beszerzése
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Ez a parancs az aktuális dátumtól/időponttól számított 7 napon belül a megadott erőforráscsoporthoz tartozó eseményeket a legtöbb 1000 jeleníti meg.

### 10. példa: erőforrás-csoport eseménynaplójának beszerzése maximális számú eseménnyel
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Ez a parancs az aktuális dátumtól/időponttól számított 7 napig lezajlott, a megadott erőforráscsoporthoz tartozó 100-eseményekre vonatkozóan jeleníti meg a legtöbbet.

### 11-es példa: az erőforráscsoport eseménynaplójának beszerzése kezdési időponttal
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Ez a 1000 parancs a megadott erőforráscsoporthoz tartozó, a 2017-05-22T04:30:00 helyi idő alatt vagy azt követően, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.

### 12 példa: az erőforráscsoport eseménynaplójának beszerzése kezdési és befejezési időponttal
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Ez a 1000 parancs a megadott erőforráscsoporthoz tartozó, a 2017-04-15T04:30 helyi idő után vagy a 2017-04-25T12:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz a megtartási időszakból.

### Példa 13: erőforrás-AZONOSÍTÓval rendelkező esemény naplózása
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Ez a parancs a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.

### 14 példa: erőforrás-AZONOSÍTÓval beolvashatja az eseménynaplót, az események maximális száma
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Ez a parancs a megadott erőforrás-AZONOSÍTÓval társított legtöbb 100-eseményen felsorolja az aktuális dátumtól/időponttól számított 7 napot.

### 15. példa: erőforrás-AZONOSÍTÓval rendelkező Eseménynapló beszerzése kezdési időponttal
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Ezek a parancsok a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen, illetve 2017-05-22T04:30:00 helyi idő szerint jelennek meg, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.

### Példa 16: erőforrás-AZONOSÍTÓval rendelkező Eseménynapló beszerzése kezdési és befejezési időponttal
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Ebben a parancsban a megadott erőforrás-AZONOSÍTÓval társított legtöbb 1000-eseményen (a 2017-04-15T04:30 helyi időpontban) vagy a 2017-04-25T12:30 helyi idő alatt, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: a retenciós időszak.

### Példa 17: erőforrás-szolgáltató eseménynaplójának beszerzése
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményen, az aktuális dátumtól és időponttól számított 7 nap volt látható.

### 18. példa: az erőforrás-szolgáltató eseménynaplójának beszerzése maximális számú eseménnyel
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 100-eseményen, az aktuális dátumtól és időponttól számított 7 nap volt látható.

### 19. példa: erőforrás-szolgáltató eseménynaplójának beszerzése kezdési időponttal
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Ez a parancs a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményen, illetve 2017-05-22T04:30:00 helyi idő alatt, ha a kezdési idő nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.

### 20 példa: az erőforrás-szolgáltató eseménynaplójának beszerzése kezdési és befejezési időponttal
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Ebben a parancsban a megadott erőforrás-szolgáltatóval társított legtöbb 1000-eseményre vonatkozóan a 2017-04-15T04:30 helyi idő, de a 2017-04-25T12:30 helyi idő, ha a teljes dátum/idő tartománya nem régebbi, mint 90 nap az aktuális dátumtól/időponttól, azaz: az adatmegőrzési időszak.

## PARAMÉTEREK

### -Hívó
A hívót adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzióhttp://www.skype.com/hu/Business/Skype-for-Business/onedrive
A korrelációs azonosítót adja meg.
Ehhez a paraméterhez szükség van.

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetailedOutput
Azt jelzi, hogy ez a parancsmag részletes kimenetet jelenít meg.
A program alapértelmezés szerint összesíti a kimenetet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -A befejezési időpont
A lekérdezés befejezési időpontját adja meg helyi időben.
Az alapértelmezett érték az aktuális idő.
Az értéknek a kezdésnél *StartTime* későbbinek kell lennie.
A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
A megadott szűrőhöz beolvasott rekordok teljes számát adja meg.
Az alapértelmezett érték a 1000, a maximálisan elfogadott érték pedig 100000. A program figyelmen kívül hagyja a negatív értékeket és a 0 értéket, és az alapértelmezett értéket fogja használni.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Az erőforrás-szolgáltató szerinti szűrést adja meg.

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kezdő időpont
A lekérdezés kezdési időpontját adja meg helyi időben.
Az alapértelmezett érték a *befejezési* hét napja mínusz.
A Get-Date parancsmaggal **datetime** -objektumot is beszerezhet.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
Az állapotot adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

### System. Management. Automation. SwitchParameter

### System. Int32

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSEventData

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
