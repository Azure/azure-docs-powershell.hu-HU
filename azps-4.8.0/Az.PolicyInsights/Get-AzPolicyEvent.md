---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184024"
---
# Get-AzPolicyEvent

## Áttekintés
Az erőforrások létrehozásakor vagy frissítésekor létrehozott házirend-értékelő eseményeket kapja.

## SZINTAXISA

### SubscriptionScope (alapértelmezett)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope paraméternél
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az erőforrások létrehozásakor vagy frissítésekor létrehozott házirend-értékelő eseményeket kapja. A házirend-esemény rekordjait különböző hatókörökben lehet lekérdezni a megadott időintervallumok (az alapértelmezett utolsó nap) alapján. Az eredmények szűréssel, csoportosítással és csoportosítási lehetőségekkel is kiszámíthatók.

## Példák

### 1. példa: házirend-események beolvasása a jelenlegi előfizetési tartományban
```powershell
PS C:\> Get-AzPolicyEvent
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.

### 2. példa: házirend-események beolvasása a megadott előfizetési tartományba
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

A megadott előfizetésben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.

### 3. példa: házirend-események beolvasása a felügyeleti csoport hatókörében
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

A megadott felügyeleti csoport összes erőforrásának utolsó napján generált házirend-esemény rekordjait kapja.

### Példa 4: házirend-események beolvasása az erőforráscsoport hatókörében a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoporthoz tartozó összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja (az előfizetésben a jelenlegi munkamenet-környezetben).

### Példa 5: házirend-események beolvasása az erőforráscsoport hatókörében a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoporthoz tartozó összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja (a megadott előfizetésben).

### Példa 6: házirend-események beszerzése egy erőforráshoz
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

A megadott erőforrás utolsó napján generált házirend-esemény rekordjait kapja.

### 7. példa: házirend-események beolvasása egy házirend-definíciós definícióban a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó nap során az összes erőforrás (a bérlői fiók jelenlegi környezetében) által generált házirend-esemény rekordjait kapja meg (ez az előfizetésben a jelenlegi munkamenet-környezetben létezik).

### 8. példa: házirend-események beolvasása a megadott előfizetéshez beállított házirend-definícióban
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői környezetben), amelyet a megadott házirend-készlet definíciója (amely a megadott előfizetésben létezik).

### Példa 9: házirend-események beolvasása egy házirend-definícióra a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői környezetben), amelyet a megadott házirend-definíció (amely az előfizetésben létezik a jelenlegi munkamenet-környezetben).

### 10. példa: házirend-események beolvasása a megadott előfizetésben lévő házirend-definícióhoz
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirend-definíció (amely a megadott előfizetésben található) minden erőforrásnál (az aktuális munkamenetben) szereplő összes erőforrás utolsó napján keletkezett házirend-esemény rekordjait kapja.

### 11-es példa: házirend-hozzárendelések beszerzése a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői környezetben), amelyet a megadott házirend-hozzárendelés (amely az előfizetésben létezik a jelenlegi munkamenet-környezetben).

### 12 példa: házirend-események beszerzése a megadott előfizetésben szereplő házirend-hozzárendeléshez
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendeléssel (amely a megadott előfizetésben található) minden erőforrás esetében az utolsó napon generált házirend-esemény rekordjait kapja.

### Példa: házirend-események beszerzése az aktuális előfizetéshez megadott erőforráscsoport házirend-hozzárendeléseihez
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Az utolsó nap során generált házirend-esemény rekordjait kapja (az aktuális munkamenetben a bérlői kontextusban), amelyet a megadott házirend-hozzárendelés (amely az előfizetéshez tartozó erőforrás csoportban található) adott meg.

### 14 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, a OrderBy, a felső és a lekérdezési beállítások megadása
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja. A parancs időbélyegző és házirend-hozzárendelési név tulajdonságai szerint rendeli az eredményeket, és az adott sorrendben szereplő adatok közül csak az 5-öt veszi át.
Azt is megadhatja, hogy csak az egyes rekordok oszlopait szeretné megjeleníteni.

### 15 példa: házirend-események beolvasása a jelenlegi előfizetési tartományból, a feladó és a lekérdezés beállításaival
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Az előfizetésben az összes erőforráshoz megadott időtartományon belül az aktuális munkamenet-környezetben megjelenő házirend-esemény rekordjait kapja.

### 16 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, a szűrő lekérdezése beállítással
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja.
A parancs a házirend-definíciós művelet (beleértve a Megtagadás vagy a naplózási műveletek) és az erőforrás hely szerinti szűréssel visszaadott eredményeket korlátozza (a eastus helyének kizárása).

### 17 példa: házirend-események beolvasása a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjainak számát kapja meg.
A parancs csak a AdditionalProperties tulajdonságban megadott házirend-esemény rekordjainak számát adja eredményül.

### 18 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, az összesítéssel való csoportosítást alkalmazva
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja. A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (csak a naplózási és elutasítási eseményeket tartalmazza) korlátozza.
A házirend-hozzárendelés, a házirend-definíció, a házirend-definíciós műveletek és az erőforrás-azonosító alapján csoportosítja az eredményeket, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.
Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.

### 19 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, az Összesítés nélküli csoportosítás megadása
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja. A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (csak a naplózási és elutasítási eseményeket tartalmazza) korlátozza.
Az eredmény az erőforrás-azonosító alapján csoportosítja a találatokat. Ezzel létrehozhatja az előfizetésben szereplő összes erőforrás listáját, amely egy házirend-eseményt generált legalább egy naplózási vagy elutasítási házirendhez.

### 20 példa: házirend-események beolvasása a jelenlegi előfizetési tartományba, a több csoportra vonatkozó meghatározás alkalmazása
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált házirend-esemény rekordjait kapja. A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (csak a Megtagadás eseményeket tartalmazza) korlátozza.
Az eredményeket először a házirend-hozzárendelés, a házirend-definíció és az erőforrás-azonosító alapján csoportosítja. Ezután az erőforrás-azonosító kivételével továbbra is csoportosítja a csoportosítás eredményét, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.
Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.
Ez a Top 5 tiltó házirendet hozza létre a legtöbb megtagadott erőforrással.

## PARAMÉTEREK

### -Apply (alkalmazás)
A kifejezés alkalmazása az összesítésekre a OData jelöléssel.

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
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Szűrő
A kifejezés szűrése OData jelöléssel

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

### -From
Az ISO 8601 formázott időbélyegző adja meg a lekérdezni kívánt intervallum kezdési időpontját.
Ha nincs megadva, az alapértelmezett érték "to" paraméterérték mínusz 1 nap.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
A felügyeleti csoport neve.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
A kifejezés megrendelése OData jelöléssel
Egy vagy több vesszővel elválasztott oszlop neve, amely nem kötelező "desc" (alapértelmezett) vagy "ASC".

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

### -PolicyAssignmentName
Házirend-hozzárendelés neve

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
Házirend-definíció neve

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
Házirend-definíció neve

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Erőforrás-azonosító.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Válassza a
Jelölje ki a kifejezést a OData jelöléssel.
Egy vagy több pontosvesszővel tagolt oszlop neve.
Az egyes rekordok oszlopait csak a kért értékekre korlátozhatja.

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

### -SubscriptionId
Előfizetés azonosítója

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
ISO 8601 formázott időbélyegző a lekérdezési intervallum befejezési időpontjának megadásával.
Ha nincs megadva, az alapértelmezett beállítás a kérés időpontjában.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
A visszaadni kívánt rekordok maximális száma

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. PolicyInsights. models. PolicyEvent

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
