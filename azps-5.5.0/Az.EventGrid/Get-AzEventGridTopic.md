---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161659"
---
# Get-AzEventGridTopic

## SYNOPSIS
Lejátsa az Eseményrács témakör részleteit, vagy az aktuális Azure-előfizetés eseményrács-témakörének listáját.

## SZINTAXIS

### ResourceGroupNameParameterSet (alapértelmezett)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A Get-AzEventGridTopic parancsmag vagy egy megadott Eseményrács-témakör adatait, vagy az aktuális Azure-előfizetés eseményrács-témakörének listáját kapja meg.
Ha a témakör neve meg van adni, akkor a rendszer egyetlen eseményrácstémát ad vissza.
Ha a témakör neve nem szerepel a listában, a visszaadott témakörlista fog visszakerülni. A listában visszaadott elemek számát a Felső paraméter vezérli. Ha a felső érték nincs megadva vagy nincs $null, a lista az összes témakörelemet tartalmazza. Ellenkező esetben a Top a listában visszaadott elemek maximális számát jelzi.
Ha továbbra is elérhetők további témakörök, a következő hívásban a NextLink értékét kell használnia a témakörök következő lapjára való bejedhez.
Végül az ODataQuery paramétert használjuk a keresési eredmények szűréséhez. A szűrő lekérdezés csak a Name tulajdonságot használó OData szintaxist követi. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

A \` \` MyResourceGroupName erőforráscsoport Eseményrács témakörÉnek Topic1 \` részét \` tartalmazza.

### 2. példa
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

A \` MyResourceGroupName erőforráscsoport Eseményrács témakörÉnek \` 1. \` témakörének részleteit \` tartalmazza.

### 3. példa
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

A MyResourceGroupName erőforráscsoport összes eseményrács-témakörének felsorolása \` \` tördelés nélkül.

### 4. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

List the first 10 Event Grid topics (if any) in resource group \` MyResourceGroupName \` that satisfes the $odataFilter query. Ha több találat érhető el, a $result. A NextLink nem lesz $null. A témakörök következő oldalának lehívása érdekében a felhasználó várhatóan újra hívja a Get-AzEventGridTopic és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

### 5. példa
```powershell
PS C:\> Get-AzEventGridTopic
```

Az előfizetés összes eseményrács-témakörének felsorolása tördelés nélkül.

### 6. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

List the first 10 Event Grid topics (if any) in the subscription that satisfes the $odataFilter query. Ha több találat érhető el, a $result. A NextLink nem lesz $null. A témakörök következő oldalának lehívása érdekében a felhasználó várhatóan újra hívja a Get-AzEventGridTopic és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Name
EventGrid-témakör neve.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
A következő behozni szükséges erőforrások lapjára mutató hivatkozás. Ezt az értéket az első parancsmag-Get-AzEventGrid akkor lehet beszerezni, ha még több erőforrás áll rendelkezésre a lekérdezhető erőforrásokhoz.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
A lista eredményeinek szűréséhez használt OData-lekérdezés. A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az Eseményrács témakört képviselő erőforrás-azonosító.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
A lekért erőforrások maximális száma. Az érvényes érték 1 és 100 között lehet. Ha a felső érték meg van adva, és további eredmények is elérhetők, az eredményben egy hivatkozás fog jelenni, amely a következő lekérdezni fogja a NextLinkben lekérdezni fogja a következő lapot. Ha nincs megadva a felső érték, a teljes erőforráslistát egyszerre adja vissza a visszaadott érték.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## KIMENETEK

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
