---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188069"
---
# Get-AzPolicyStateSummary

## Áttekintés
A legújabb házirend-megfelelőségi állapotok összegzése az erőforrásokhoz.

## SZINTAXISA

### SubscriptionScope (alapértelmezett)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope paraméternél
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A házirend-hozzárendelések és a házirend-definíciók szerint részletezett, a legutóbb követett házirend-megfelelőségi állapotokat tartalmazó összefoglaló nézetet kapja. Csak a nem megfelelő házirend-állapotokat tartalmazza.

## Példák

### Példa 1: a legújabb, nem kompatibilis házirend-Államok összefoglalása a jelenlegi előfizetési tartományba
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg.

### 2. példa: a legújabb, nem kompatibilis házirend-Államok összegzésének beszerzése a megadott előfizetési tartományba
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

A megadott előfizetésben szereplő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja.

### 3. példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a felügyeleti csoport hatókörében
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Az utolsó napon az adott kezelési csoportban található összes erőforrás utolsó napján generált házirend-megfelelőségi állapotának összefoglaló nézetét kapja.

### Példa 4: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése az erőforráscsoport hatókörében a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Az utolsó napon a megadott erőforráscsoport összes erőforrásának utolsó napján generált házirend-megfelelőségi állapot összefoglaló nézetét kapja (az előfizetésben a jelenlegi munkamenet-környezetben).

### Példa 5: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése az erőforráscsoport hatókörében a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Az utolsó napon a megadott erőforráscsoport (a megadott előfizetés) összes erőforrásának utolsó napján generált házirend-megfelelőségi állapotának összefoglaló nézetét kapja.

### Példa 6: a legkésőbbi, nem kompatibilis házirend-Államok összefoglalójának beszerzése erőforráshoz
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

A megadott erőforrás utolsó napján generált házirend-megfelelőségi országok összefoglaló nézetét kapja meg.

### 7. példa: a legutóbb nem kompatibilis házirend-állapotok összefoglalása egy házirend-készlet definíciójában a jelenlegi előfizetésben
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az aktuális munkamenetben az előfizetésben szereplő összes erőforrás (az aktuális munkamenet kontextusában megtalálható) utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg.

### 8. példa: a legutóbb nem kompatibilis házirend-állapotok összefoglalása a megadott előfizetéshez tartozó házirend-definíciós definícióban
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Az utolsó napon az összes erőforrás (az aktuális munkamenetben a bérlőn belül) által generált utolsó, az utolsó napon létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja meg (amely a megadott előfizetésben található).

### Példa 9: a legújabb, nem kompatibilis házirend-Államok összefoglalása a jelenlegi előfizetés házirend-definíciójának összegzése
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A legutóbbi, az előfizetésben az aktuális munkamenet kontextusában található (az előfizetésben a jelenlegi munkamenetben) által megvalósított összes erőforrás utolsó napján generált, a legutóbb létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja.

### 10. példa: a legújabb, nem kompatibilis házirend-állapotok összefoglalása a megadott előfizetésben lévő házirend-definícióhoz
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Megtekintheti a legutóbbi, a megadott házirend-definícióval (a megadott előfizetésben található) erőforrásokkal (az aktuális munkamenetben a bérlőn belül) az összes erőforrás utolsó napján létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét.

### 11. példa: a legutóbb nem kompatibilis házirendek összegzése a meglévő előfizetésben lévő házirend-hozzárendeléshez
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A legutóbbi, az előfizetésben az aktuális munkamenet kontextusában megtalálható erőforrás-hozzárendelések utolsó napján létrehozott, a legutóbb létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja.

### 12. példa: a legutóbb nem kompatibilis házirend-állapotok összefoglalása a megadott előfizetéshez tartozó házirend-hozzárendeléshez
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Az utolsó napon létrehozott, a legutóbb létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja meg a megadott házirend-hozzárendeléssel (amely a megadott előfizetésben létezik).

### 13. példa: az aktuális előfizetéshez tartozó meghatározott erőforráscsoport házirend-hozzárendeléseinek összefoglalása a legutóbb nem megfelelő házirend-hozzárendelésekkel
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Az aktuális munkamenetben az előfizetésben szereplő erőforrás-hozzárendelésben (az aktuális munkamenet-környezetben) az összes erőforrás utolsó napján létrehozott, a legutóbb létrehozott házirendek megfelelőségi állapotának összefoglaló nézetét kapja.

### 14 példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a jelenlegi előfizetési tartományba, a felső lekérdezés beállítással
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg. A parancs a házirend-hozzárendelés összefoglalóit nem megfelelő erőforrásokkal rendeli az eredményben, és a házirend-hozzárendelési összesítések közül csak a legfelső 5-öt veszi figyelembe.

### 15. példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a jelenlegi előfizetési tartományba, a feladó és a lekérdezés beállításaival
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Az előfizetésben a jelenlegi munkamenet-környezetben az összes erőforráshoz megadott dátumtartomány által generált legutóbb létrehozott házirend-megfelelőségi állapotok összefoglaló nézetét kapja.

### 16. példa: a legújabb, nem kompatibilis házirend-Államok összefoglalójának beszerzése a jelenlegi előfizetési tartományba, a szűrő lekérdezése beállítással
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Az előfizetésben az aktuális munkamenetben lévő összes erőforrás utolsó napján az utolsó napon létrehozott házirend-megfelelőségi országok összefoglaló nézetét kapja meg.
A parancs a házirend-definíciós műveleteken (beleértve a Megtagadás vagy a naplózási műveleteket) alapuló szűréssel, valamint az erőforrás helyével (a eastus helyének kivételével) korlátozza a találatokat.

## PARAMÉTEREK

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

### Microsoft. Azure. Command. PolicyInsights. models. PolicyStateSummary

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPolicyState](./Get-AzPolicyState.md)
