---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481008"
---
# Get-UsageAggregates

## SYNOPSIS
Itt olvashatja be az Azure-előfizetés használati adatait.

## SZINTAXIS

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-UsageAggregates** parancsmag az alábbi tulajdonságok alapján összesíti az Azure-előfizetés használati adatait: 
- A használat bejelentésének kezdő és záró időpontja.
- Az aggregáció pontossága napi vagy óránkénti módon.
- Példányszintű részletek ugyanannak az erőforrásnak több példányához.
A konzisztens eredmény érdekében a visszaadott adatok azon alapulnak, hogy mikor jelente meg a használati adatokat az Azure-erőforrás.
További információt az Azure Billing REST API Reference https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) (a Microsoft Developer Network tárában) található.

## PÉLDÁK

### 1. példa: Előfizetési adatok beolvasása
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Ez a parancs 2015.05.02. és 2015.05.05. között olvassa be az előfizetés használati adatait.

## PARAMETERS

### -AggregationGranularity
Az adatok összesítési pontosságát adja meg.
Érvényes értékek: Naponta és Óránként.
Az alapértelmezett érték a Naponta érték.

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Az előző hívásban a válasz törzséből beolvasott folytatási jogkivonatot adja meg.
Nagy eredményhalmaz esetén a válaszokat a folytatási jogkivonatok használatával lapelik.
A folytatási jogkivonat könyvjelzőként szolgál az előrehaladáshoz.
Ha nem adja meg ezt a paramétert, az adatok beolvasása a ReportedStartTime-ban megadott nap vagy óra *elejéről történik.*
Azt javasoljuk, hogy az adatokkal együtt kövesse a lapra adott válasz következő hivatkozását.

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

### -ReportedEndTime
Megadja az Erőforrás-használat Azure számlázási rendszerben való rögzítésekor jelentett záró időt.
Az Azure egy elosztott rendszer, amely világszerte több adatközpontot is áttűn, így késéssel számolhat az erőforrás-felhasználás ideje , vagyis az erőforrás kihasználtsága és a számlázási rendszer elérése között( ez az erőforrás-használat által jelentett idő).
Az előfizetés adott időszakra jelentett összes használati eseményének lekérdezése a jelentett idő alapján történt.
Bár a lekérdezést a jelentett idő alapján kell lekérdezni, a parancsmag összesíti a válaszadatokat az erőforrás kihasználtsága szerint.
Az erőforrás-használati adatok hasznos kimutatások az adatok elemzéséhez.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Megadja az Erőforrás-használat Azure számlázási rendszerben való rögzítésekor jelentett kezdési időt.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
Azt jelzi, hogy a parancsmag példányszintű adatokat ad-e vissza a használati adatokkal együtt.
Az alapértelmezett érték $True.
Ha $False, a szolgáltatás összesíti az eredményeket a kiszolgáló oldalán, és így kevesebb összesítő csoportot ad vissza.
Ha például három webhelyet futtat, alapértelmezés szerint három sort fog kapni webhely-használatra.
Ha azonban az értéket $False, az ugyanannak az **előfizetésiIdnek,** a **meterIdnek,** a **usageStartTime-nak** és a **usageEndTime-nak** az összes adata egysoros elemként lesz összecsukva.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
