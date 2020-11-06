---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: e3bfdd771413f17d4dd560a350d45fdb3f47c5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493715"
---
# Invoke-AzureRmOperationalInsightsQuery

## Áttekintés
A megadott paraméterek alapján adja eredményül a találatokat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByWorkspaceId (alapértelmezett)
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **meghívó-AzureRmOperationalInsightsQuery** parancsmag a megadott paraméterek alapján adja eredményül a találatokat.

A keresés állapotát a visszaadott objektum metaadat tulajdonságában érheti el.
Ha az állapot függőben van, akkor a keresés nem fejeződött be, és az eredmény az archívumból fog szerepelni.

A keresés eredményét a visszaadott objektum Value tulajdonságában olvashatja le.

## Példák

### 1. példa: keresési eredmények lekérdezéssel történő beszerzése
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

A meghívást követően a $queryResults. Results a lekérdezésből származó összes sort fogja tartalmazni.

### 2. példa: $results konvertálása Eredmény IEnumberable egy tömbhöz
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

Egyes lekérdezések nagyon nagy mennyiségű adatkészletet adhatnak eredményül. Emiatt a parancsmag alapértelmezett viselkedése egy IEnumerable visszaadása a memória költségeinek csökkentéséhez. Ha a találatok tömbjét szeretné használni, a LINQ enumerable. ToArray () kiterjesztési módszerrel konvertálhatja a IEnumerable tömböra.

### 3. példa: a keresési eredmények lekérdezése meghatározott időkereten keresztüli lekérdezéssel
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

A lekérdezés eredményei az elmúlt 24 órára korlátozódnak.

### Példa 4: a lekérdezés eredményében megjelenített & statisztikájának befoglalása
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

További információt a [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) Megjelenítés és a statisztikai adatok című témakörben találhat.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben
```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeRender
Ha meg van adva, akkor a metrika-lekérdezések megjelenítési adatai is szerepelni fognak a válaszban.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeStatistics
Ha meg van adva, a lekérdezés statisztikája is szerepelni fog a válaszban.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
A végrehajtandó lekérdezés.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Időszak
A lekérdezés által kötött időszak.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Várjon
Felső határt ad arra az időmennyiségre, amikor a kiszolgáló a lekérdezés feldolgozását fogja tölteni.
Olvassa el https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Munkaterület
A munkaterület

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceId
A munkaterület-azonosító.

```yaml
Type: String
Parameter Sets: ByWorkspaceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace
Ha a vezetékes elem be van jelentkezve, a program Kinyeri a munkaterület AZONOSÍTÓját a PSWorkspace. Egyéb esetben a workspaceId paraméterrel manuálisan is megadhatja a munkaterület-azonosítót.

## KIMENETEK

### Microsoft. Azure. Command. OperationalInsights. models. PSQueryResponse
A ***PSQueryResponse*** a lekérdezés eredményét jeleníti meg & statisztikát.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

