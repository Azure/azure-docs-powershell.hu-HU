---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343410"
---
# Get-AzActivityLog

## SYNOPSIS
Tevékenységnapló-események beolvasása.

## SZINTAXIS

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A Get-AzActivityLog parancsmag beolvassa a tevékenységnapló eseményeit. Az események az aktuális előfizetés-azonosítóhoz, korrelációs azonosítóhoz, erőforráscsoporthoz, erőforrás-azonosítóhoz vagy erőforrás-szolgáltatóhoz társíthatók.

## PÉLDÁK

### 1. példa: Eseménynapló lekérte előfizetésazonosító szerint
```
PS C:\>Get-ActivityAzLog
```

Ez a parancs a felhasználó előfizetés-azonosítójával társított legtöbb 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.

### 2. példa: Eseménynapló lekérte az előfizetésazonosítót, amely maximális számú eseményt adott meg
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Ez a parancs a felhasználó előfizetés-azonosítójával társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.

### 3. példa: Eseménynapló lekérte az előfizetés azonosítóját kezdési időpontban.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Ez a parancs a 2017-06-06-01T10:30 időpontban helyi idő szerint 2017-06-01T10:30 időpontban megadott felhasználó előfizetés-azonosítójával társított legtöbb 1000 eseményt sorolja fel, ha az adott dátum/idő nem régebbi az aktuális dátumtól/időponttól 90 napnál.

### 4. példa: Eseménynapló lekérte előfizetésazonosító alapján kezdési és záró időpontra.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Ez a parancs a 2017-04-04-01T10:30 helyi időpontban, illetve a 2017-04-14T11:30 időpontban, illetve a 2017-04-14T11:30 időpontig helyi idő előtt, ha a teljes dátum/időtartomány nem régebbi az aktuális dátumtól/időponttól ( például a megőrzési időtől) 1000-ig.

### 5. példa: Eseménynapló lekérte korrelációs azonosító alapján
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Ez a parancs a legtöbb 1000 eseményt sorolja fel a megadott korrelációs azonosítóval, amely az aktuális dátumtól/időponttól 7 nappal történt. 
**MEGJEGYZÉS:** ez általában csak egy esemény.

### 6. példa: Eseménynapló lekérte korrelációs azonosító alapján, maximális számú esemény esetén
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Ez a parancs a megadott korrelációs azonosítóval társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek. 
**MEGJEGYZÉS:** ez általában csak egy esemény.

### 7. példa: Eseménynapló lekérte korrelációs azonosító és kezdési időpont alapján
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Ez a parancs a 2017–05–22T04:30:00 időpontban megadott korrelációs azonosítóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.
**MEGJEGYZÉS:** ez általában csak egy esemény.

### 8. példa: Eseménynapló lekérte korrelációs azonosító alapján a kezdési és a záró időpontmal
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Ez a parancs a 2017–04–15T04:30 helyi időtartományon vagy azt követően lekért korrelációs azonosítóval társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).

### 9. példa: Erőforráscsoport eseménynaplója
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Ez a parancs legalább 1000 olyan eseményt sorol fel, amely a megadott erőforráscsoporthoz tartozik, és az aktuális dátumtól/időponttól 7 nappal történt.

### 10. példa: Eseménynapló bejedése egy legfeljebb eseményszámú erőforráscsoporthoz
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Ez a parancs a megadott erőforráscsoporttal társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.

### 11. példa: Erőforráscsoport eseménynaplója kezdési időpontra
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Ez a parancs a 2017–05–22T04:30:00 időpontban megadott erőforráscsoporttal társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.

### 12. példa: Eseménynapló lekérte egy kezdési és a záró időponttal egy erőforráscsoporthoz
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Ez a parancs a 2017-04-15T04:30 helyi időtartományon vagy azt követően a megadott erőforráscsoporttal társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).

### 13. példa: Eseménynapló lekérte erőforrás-azonosító szerint
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Ez a parancs a megadott erőforrás-azonosítóhoz tartozó 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.

### 14. példa: Eseménynapló lekérte erőforrás-azonosító szerint, maximális számú esemény esetén
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Ez a parancs a megadott erőforrás-azonosítóhoz tartozó 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.

### 15. példa: Eseménynapló lekérte erőforrás-azonosítója alapján kezdési időpont esetén
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Ez a parancs a 2017–05–22T04:30:00 helyi időtartományban megadott erőforrás-azonosítóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.

### 16. példa: Eseménynapló lekérte erőforrás-azonosító szerint kezdési és záró időpont esetén
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Ez a parancs a 2017–04–15T04:30 helyi időtartományon vagy azt követően lekért erőforrás-azonosítóval társított legtöbb 1000 eseményt sorolja fel, de a 2017-04-25T12:30 időpont előtt, ha a teljes dátum/időtartomány nem régebbi 90 napnál az aktuális dátumtól/időponttól( vagyis a megőrzési időszaktól).

### 17. példa: Eseménynapló lekérte az erőforrás-szolgáltató
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Ez a parancs a megadott erőforrás-szolgáltatóval társított 1000 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.

### 18. példa: Eseménynapló lekérte az erőforrás-szolgáltató által, amely maximális számú eseményt tud behozni
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Ez a parancs a megadott erőforrás-szolgáltatóval társított 100 eseményt sorolja fel, amelyek az aktuális dátumtól/időponttól 7 nappal történtek.

### 19. példa: Eseménynapló lekérte az erőforrás-szolgáltatótól kezdési időpontban
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Ez a parancs a 2017–05–22T04:30:00 időpontban megadott erőforrás-szolgáltatóval társított legtöbb 1000 eseményt sorolja fel, ha a kezdési időpont nem régebbi, mint 90 nap az aktuális dátumtól/időponttól.

### 20. példa: Eseménynapló beása erőforrás-szolgáltató szerint kezdési és záró időpontban
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Ez a parancs a 2017–2017–04–15T04:30 helyi időtartományon, de a 2017-04-25T12:30 időpontig helyi idő előtt, ha a teljes dátum/időtartomány nem régebbi, mint 90 nap az aktuális dátumtól/időponttól (vagyis a megőrzési időszaktól) társított 1000 esemény.

## PARAMETERS

### -Hívó
A lehívni megfelelő események hívója

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

### -CorrelationId
The CorrelationId

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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
A Return objektum az események összes adatával együtt (az alapértelmezett érték az, hogy csak bizonyos attribútumokat ad vissza, azaz nem ad részletes adatokat)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
The endTime of the query

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
A lehívni megfelelő rekordok maximális száma.
Alias: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve

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
A ResourceId

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
A ResourceProvider neve

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

### -StartTime
A lekérdezés korrelációsazonosítója

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
A lehívni megfelelő események állapota

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## KIMENETEK

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
