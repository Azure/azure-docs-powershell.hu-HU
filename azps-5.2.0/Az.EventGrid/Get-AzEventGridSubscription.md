---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329610"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Lekérte egy esemény-előfizetés adatait, vagy lekérte az aktuális Azure-előfizetés összes esemény-előfizetésének listáját.

## SZINTAXIS

### EventSubscriptionTopicNameParameterSet (alapértelmezett)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A Get-AzEventGridSubscription parancsmag vagy egy megadott Event Grid-előfizetés adatait, vagy az aktuális Azure-előfizetés vagy -erőforráscsoport eseményrács-előfizetésének listáját kapja.
Ha meg van biztosítanak egy esemény-előfizetés nevét, a rendszer visszaadja egyetlen Eseményrács-előfizetés adatait.
Ha az esemény-előfizetés neve nem szerepel, a visszaadott érték az összes esemény-előfizetés listája lesz. A listában visszaadott elemek számát a Felső paraméter vezérli. Ha a felső érték nincs megadva vagy nincs $null, a lista az összes esemény-előfizetési elemet tartalmazza. Ellenkező esetben a Top a listában visszaadott elemek maximális számát jelzi.
Ha még több esemény-előfizetés áll rendelkezésre, a NextLink értékét a következő hívásban kell használnia az esemény-előfizetések következő lapjára való feliratkozáshoz.
Végül az ODataQuery paramétert használjuk a keresési eredmények szűréséhez. A szűrő lekérdezés csak a Name tulajdonságot használó OData szintaxist követi. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Az EventSubscription1 esemény-előfizetés adatait tartalmazza, amely a \` \` \` \` MyResourceGroupName erőforráscsoport Topic1 témaköréhez \` \` készült.

### 2. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

A MyResourceGroupName erőforráscsoporthoz létrehozott EventSubscription1 esemény-előfizetés adatait tartalmazza, beleértve a teljes végpont URL-címét, ha \` \` \` \` \` \` webhook-alapú esemény-előfizetésről van szükség.

### 3. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

A MyResourceGroupName erőforráscsoport Topic1 témaköréhez létrehozott összes esemény-előfizetés listája \` \` \` \` tördelés nélkül.

### 4. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

List the first 10 event subscriptions (if any) created for \` topic Topic1 \` in resource group \` MyResourceGroupName \` that satesfes the $odataFilter query. Ha több találat érhető el, a $result. A NextLink nem lesz $null. Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

### 5. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

A \` \` \` MyResourceGroupName erőforráscsoporthoz létrehozott EventSubscription1 esemény-előfizetés adatait \` tartalmazza.

### 6. példa
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Az aktuálisan kijelölt Azure-előfizetéshez létrehozott \` EventSubscription1 \` esemény-előfizetés adatait tartalmazza.

### 7. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

A MyResourceGroupName erőforráscsoport alatt létrehozott összes globális esemény-előfizetés listáját \` \` tördelés nélkül beveszi.

### 8. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Sorolja fel a MyResourceGroupName erőforráscsoportban létrehozott első 5 esemény-előfizetést (ha van ilyen), amely megfelel a $odataFilter \` \` lekérdezésnek. Ha több találat érhető el, a $result. A NextLink nem lesz $null. Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

### 9. példa
```powershell
PS C:\> Get-AzEventGridSubscription
```

A jelenleg kijelölt Azure-előfizetés alatt létrehozott összes globális esemény-előfizetés listáját tördelés nélkül lejátssa.

### 10. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Sorolja fel az aktuálisan kiválasztott Azure-előfizetés alatt létrehozott első 15 globális esemény-előfizetést (ha van ilyen), amely megfelel a $odataFilter lekérdezésnek. Ha több találat érhető el, a $result. A NextLink nem lesz $null. Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

### 11. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

A MyResourceGroupName erőforráscsoportban létrehozott összes regionális esemény-előfizetés listáját a \` \` megadott \` helyen, a westus2 helyen, tördelés nélkül \` adja meg.

### 12. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

List the first 15 regional event subscriptions (if any) created under resource group \` MyResourceGroupName \` in the specified location westus2 that \` \` satisfes the $odataFilter query. Ha több találat érhető el, a $result. A NextLink nem lesz $null. Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

### 13. példa
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Tördelés nélkül beveszi a megadott EventHub névtérhez létrehozott összes esemény-előfizetés listáját.

### 14. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfes the $odataFilter query. Ha több találat érhető el, a $result. A NextLink nem lesz $null. Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

### 15. példa
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

A megadott témakörtípushoz (EventHub névterek) létrehozott összes esemény-előfizetés listáját tördelés nélkül beveszi a megadott helyen.

### 16. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfes the $odataFilter query. Ha több találat érhető el, a $result. A NextLink nem lesz $null. Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

### 17. példa
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Tördelés nélkül beveszi az adott erőforráscsoporthoz létrehozott összes esemény-előfizetés listáját.

### 18. példa
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

List the first 100 event subscriptions (if any) created for the specific resource group that satesfes the $odataFilter query. Ha több találat érhető el, a $result. A NextLink nem lesz $null. Az esemény-előfizetések következő oldalának lehívásához a felhasználó várhatóan újra hívja Get-AzEventGridSubscription és az eredményt használja. Az előző hívásból kapott NextLink. A hívónak meg kell állnia, amikor az eredmény álljon meg. A NextLink $null.

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

### -DomainInputObject
EventGrid Domain objektum.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
EventGrid tartománynév.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
EventGrid domain Topic objektum.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
EventGrid tartomány témakörének neve.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Az esemény-előfizetés neve

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Tartalmazza az esemény-előfizetés célhelyének teljes végpont URL-címét.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid Topic objektum.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Hely

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Annak az erőforrásnak az azonosítója, amelyhez esemény-előfizetések létrejöttek.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
A lista eredményeinek szűréséhez használt OData-lekérdezés. A szűrés jelenleg csak a Név tulajdonságban engedélyezett. A támogatott műveletek közé tartoznak a következők: CONTAINS, eq (egyenlő), ne (nem egyenlő), ÉS, VAGY és NEM.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
EventGrid-témakör neve.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType name

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
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

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## KIMENETEK

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
