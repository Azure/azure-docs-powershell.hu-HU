---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012979"
---
# Get-AzPolicyState

## Áttekintés
Házirend-megfelelőségi állapotokat kap az erőforrásokhoz.

## SZINTAXISA

### SubscriptionScope (alapértelmezett)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope paraméternél
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Házirend-megfelelőségi állapotokat kap az erőforrásokhoz. A házirend-állam rekordjait több hatókörben is lekérdezheti. A megadott időintervallumon (alapértelmezett esetben az utolsó napon) alapulva lekérdezheti, hogy a legutóbbi házirendek vagy az összes házirend-állam áttűnése elérhető-e. Az eredmények szűréssel, csoportosítással és csoportosítási lehetőségekkel is kiszámíthatók.

## Példák

### Példa 1: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba
```powershell
PS C:\> Get-AzPolicyState
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.

### 2. példa: a legutóbbi házirend-állapot beszerzése a megadott előfizetési tartományba
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

A megadott előfizetésben lévő összes erőforrás utolsó napján generált legutóbb létrehozott házirend-nyilvántartási rekordokat kapja.

### 3. példa: az összes házirend-állapot beolvasása a jelenlegi előfizetési tartományba
```powershell
PS C:\> Get-AzPolicyState -All
```

Az előfizetésben a jelenlegi munkamenet-környezetben az összes erőforrás utolsó napján generált összes korábbi házirend-rekord (a legújabbat is tartalmazza).

### Példa 4: a legújabb házirendek beszerzése a felügyeleti csoport hatókörében
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Az utolsó napon az adott kezelési csoportban található összes erőforrás esetében generálta a legutóbb létrehozott házirend-nyilvántartást.

### 5. példa: a legutóbbi házirend-állapot beolvasása az erőforráscsoport hatókörében a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoport összes erőforrását (az előfizetést az aktuális munkamenet kontextusában) az utolsó napon generált házirend-nyilvántartási rekordok utolsó napján kapja meg.

### Példa 6: a legújabb házirendek beszerzése az erőforráscsoport hatókörében a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoport összes erőforrásának utolsó napján generált legutóbb létrehozott házirend-nyilvántartási rekordok (a megadott előfizetésben).

### 7. példa: a legutóbbi házirend-állapot beszerzése egy erőforráshoz
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

A megadott erőforrás utolsó napján generált naplórend-rekordokat kapja.

### 8. példa: a legutóbbi előfizetésben beállított házirend-definíciós szabályok beszerzése
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó napon az összes erőforrás (a bérlő a jelenlegi munkamenet-környezetében) által generált legújabb házirend-nyilvántartási rekordokat kapja meg (amely az előfizetésben a jelenlegi munkamenet-környezetben létezik).

### Példa 9: a legújabb házirendek beszerzése egy házirend-készlet definíciója a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó napon az utolsó napon generált házirend-nyilvántartási rekordokat kapja meg (a megadott előfizetésben megtalálható a bérlői környezeten belül).

### 10. példa: a legutóbbi előfizetéshez tartozó házirend-definíció beszerzése a legutóbbi házirendek szerint
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó napon az utolsó napon létrehozott házirend-nyilvántartási rekordok (az aktuális munkamenetben a bérlői környezetben) által megadott házirend-definícióval

### Példa: a legutóbbi házirendek beszerzése házirend-definícióra a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó napon az utolsó napon generált házirend-nyilvántartási rekordokat kapja meg (a megadott előfizetésben megtalálható) a megadott házirend-definícióval (amely a megadott előfizetésben létezik).

### 12. példa: a legutóbbi előfizetésben lévő házirend-hozzárendelés legutóbbi házirendjének beszerzése
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Az utolsó napon az utolsó napon létrehozott házirend-nyilvántartási rekordok (az aktuális munkamenetben az előfizetésben megtalálható) által megvalósított összes erőforrás (az aktuális munkamenet-környezetben)

### Példa: a legutóbbi házirendek beszerzése a megadott előfizetéshez tartozó házirend-hozzárendeléshez
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Az utolsó napon az utolsó napon generált házirend-nyilvántartási rekordokat kapja meg (a megadott előfizetésben megtalálható a bérlői környezeten belül).

### 14. példa: a legutóbbi előfizetéshez tartozó erőforráscsoport házirend-hozzárendeléséhez szükséges legutóbbi házirendek beszerzése
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Az utolsó napon az összes erőforrás (az aktuális munkamenetben a bérlői környezetben) által létrehozott, a megadott házirend-hozzárendeléssel (amely az előfizetéshez tartozó erőforrás csoportban található)

### 15. példa: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba, a OrderBy, a felső és a lekérdezési beállítások megadása
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja. A parancs időbélyegző és házirend-hozzárendelési név tulajdonságai szerint rendeli az eredményeket, és az adott sorrendben szereplő adatok közül csak az 5-öt veszi át.
Azt is megadhatja, hogy csak az egyes rekordok oszlopait szeretné megjeleníteni.

### 16. példa: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba, a lekérdezési és a lekérdezési beállításokkal
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Az előfizetésben szereplő összes erőforráshoz megadott dátumtartomány által az aktuális munkamenet-környezetben létrehozott legújabb házirend-nyilvántartásokat kapja.

### 17. példa: a legújabb házirendek beszerzése a jelenlegi előfizetési tartományba, a szűrő lekérdezése beállítással
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja.
A parancs a házirend-definíciós műveleteken alapuló szűréssel visszaadott eredményeket (beleértve a Megtagadás vagy a könyvvizsgálati műveleteket is), a megfelelőségi állapotot (csak a nem megfelelő állapotot tartalmazza) és az erőforrás helyének korlátozásával (kivéve a eastus helyét).

### 18. példa: a legutóbbi házirend-adatok beszerzése a jelenlegi előfizetési tartományba, a sor számlálási összesítésének megadása
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján generált legutóbb létrehozott házirend-rekordok számát adja eredményül.
A parancs csak a AdditionalProperties tulajdonságban megadott irányelvmodul-rekordok számát adja eredményül.

### 19. példa: a legutóbbi házirend-állapot beszerzése a jelenlegi előfizetési tartományba, az összesítéssel történő csoportosítás megadása
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja. A parancs a megfelelőségi állapoton alapuló szűréssel visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).
A házirend-hozzárendelés, a házirend-definíció és a házirend-definíció alapján csoportosítja az eredményeket, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.
Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.

### 20. példa: a legutóbbi házirend-állapot beszerzése a jelenlegi előfizetési tartományba, az Összesítés nélküli csoportosítás megadása
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja. A parancs a megfelelőségi állapoton alapuló szűréssel visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).
Az eredmény az erőforrás-azonosító alapján csoportosítja a találatokat. Ezzel létrehozhatja az előfizetéshez tartozó összes erőforrás listáját, amelyek nem felelnek meg legalább egy házirendnek.

### 21. példa: a legutóbbi házirend-állapot beszerzése a jelenlegi előfizetési tartományba
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### 22. példa: a legutóbbi házirendek beszerzése, valamint az erőforrásokra vonatkozó házirendek kiértékelésének részletei
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon generált naplórend-rekordokat kapja. A parancs a megfelelőségi állapoton alapuló szűréssel visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).
Az eredményeket először a házirend-hozzárendelés, a házirend-definíció, a házirend-definíció és az erőforrás-azonosító alapján csoportosítja. Ezután az erőforrás-azonosító kivételével továbbra is csoportosítja a csoportosítás eredményét, és kiszámítja az egyes csoportok rekordjainak számát, amelyet a AdditionalProperties tulajdonságon belül ad vissza.
Az eredményeket a darab összesítése szerint csökkenő sorrendben rendeli el, és az adott sorrendben csak a legfelső 5 értéket veszi figyelembe.
Ez a felső 5 házirendet hozza létre a nem megfelelő erőforrásokkal.

## PARAMÉTEREK

### -All (mind)
A megadott időintervallumon belül csak a legkésőbbi időpontban kapja meg az összes házirendet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### – Kibontás
A kifejezés kibontása OData jelöléssel

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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

### Microsoft. Azure. Command. PolicyInsights. models. PolicyState

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
