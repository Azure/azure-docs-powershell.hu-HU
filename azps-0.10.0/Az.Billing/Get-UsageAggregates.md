---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 510d0ee001e4c291dad3cc024f593d1f29c7ddca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840982"
---
# Get-UsageAggregates

## Áttekintés
Megkapja a bejelentett Azure-előfizetés használati adatait.

## SZINTAXISA

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-UsageAggregates** parancsmag az Azure-előfizetés használati adatainak összegzéséhez a következő tulajdonságokat kapja: 
- A felhasználás jelentésének kezdési és befejezési időpontja.
- Összesítési pontosság (naponta vagy óránként)
- Az adott erőforrás több példányának a példány szintű részletei.
Konzisztens eredmények esetén a visszaadott adatok attól függnek, hogy az Azure-erőforrás mikor jelentette a használati adatokat.
További információt az Azure számlázási REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c -hivatkozás ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) a Microsoft Developer Network Library) című témakörben talál.

## Példák

### Példa 1: előfizetés adatainak beolvasása
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Ez a parancs beolvassa az 5/2/2015 és az 5/5/2015 közötti előfizetés használati adatainak jelentését.

## PARAMÉTEREK

### -AggregationGranularity
Az érték összesítési pontosságát adja meg.
Az érvényes értékek: naponta és óránként.
Az alapértelmezett érték naponta.

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
Az előző hívás válasz törzséről lekért folytatási tokent adja meg.
Nagy eredményhalmaz esetén a válaszokat a folytatólagos tokenek segítségével lapozhatja.
A folytatási token könyvjelzőként szolgál a folyamathoz.
Ha nem adja meg ezt a paramétert, az adatai a *ReportedStartTime* megadott nap vagy óra elejétől kezdve olvashatók.
Azt javasoljuk, hogy kövesse a válasz az oldalra című következő hivatkozást, de az adatot.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Az erőforrás-használat Azure számlázási rendszerbe való felvételének bejelentett befejezési időpontját adja meg.
Az Azure egy olyan kiosztott rendszer, amely több adatközpontot tartalmaz világszerte, így az Erőforrás kihasználtsága között az Erőforrás kihasználtsága és a számlázási rendszer, amikor a használati esemény elérte a számlázási rendszert, az Erőforrás kihasználtsága időpontját jelenti.
Annak érdekében, hogy az előfizetéshez az adott időszakra bejelentett összes használati eseményt beszerezze, a lekérdezés a bejelentett idő szerint történjen.
Annak ellenére, hogy a megadott idő szerint lekérdezést kérdez le, a parancsmag összesíti a válasz adatmennyiségét az erőforrás kihasználtsági ideje alapján.
Az erőforrás-használati adatok a hasznos kimutatás az adatok elemzéséhez.

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
Megadja, hogy milyen kezdési idő legyen látható az erőforrás-használat Azure számlázási rendszerben való felvételekor.

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
Azt jelzi, hogy ez a parancsmag a használati adatokból példány-szintű részleteket ad-e eredményül.
Az alapértelmezett érték $True.
Ha $False, a szolgáltatás összesíti az eredményeket a kiszolgáló oldalán, és így kevesebb összesített csoportot ad eredményül.
Ha például három webhelyet futtat, alapértelmezés szerint három elem jelenik meg a webhely-felhasználáshoz.
Az érték $False esetén azonban minden adat ugyanahhoz a **subscriptionId** , **meterId** , **usageStartTime** és **usageEndTime** van összecsukva egyetlen sorba.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Commerce. UsageAggregates. models. UsageAggregationGetResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK