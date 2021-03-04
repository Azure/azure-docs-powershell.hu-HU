---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937545"
---
# Get-AzPolicyEvent

## SYNOPSIS
Házirend-kiértékelési eseményeket hoz létre, amikor erőforrások jönnek létre vagy frissülnek.

## SZINTAXIS

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

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
Házirend-kiértékelési eseményeket hoz létre, amikor erőforrások jönnek létre vagy frissülnek. A házirendesemény-rekordok lekérdezhetők különböző hatókörökben a megadott időintervallum alapján (ez az alapértelmezett érték az utolsó nap). Az eredmények szűrhetők, csoportosíthatóak és a csoportösszesítők számíthatóak.

## PÉLDÁK

### 1. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét
```powershell
PS C:\> Get-AzPolicyEvent
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.

### 2. példa: Házirendesemények lekérte a megadott előfizetési hatókört
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Házirendesemény-rekordokat hoz létre az utolsó napon a megadott előfizetésben található összes erőforráshoz.

### 3. példa: Házirendesemények levezetése a felügyeleti csoport hatókörében
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

A megadott felügyeleti csoport összes erőforrása számára az utolsó napon létrehozott házirend-eseményrekordokat adja vissza.

### 4. példa: Házirendesemények lekértése az aktuális előfizetés erőforráscsoport-hatókörében
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoport összes erőforrásához (az aktuális munkamenet kontextusában az előfizetéshez) az utolsó napon létrehozott házirend-eseményrekordokat kapja.

### 5. példa: Házirendesemények lekértése az erőforráscsoport hatókörében a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoport összes erőforrásához (a megadott előfizetésben) az utolsó napon létrehozott házirend-eseményrekordokat adja vissza.

### 6. példa: Házirendesemények lekérte egy erőforráshoz
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

A megadott erőforrás utolsó napján létrehozott házirendesemény-rekordokat adja vissza.

### 7. példa: Házirend-definíció házirendesemények lekértése az aktuális előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirendkészlet-definíció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.

### 8. példa: Házirend-definíció házirendesemények lekértése a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirendkészlet-definíció által (a megadott előfizetésben létező) összes erőforráshoz (a bérlő aktuális munkamenet kontextusában) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.

### 9. példa: Házirendesemények lekérte egy házirenddefinícióhoz az aktuális előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirenddefiníció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.

### 10. példa: Házirendesemények lekértése egy házirenddefinícióhoz a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirenddefiníció által (a megadott előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet környezetében a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.

### 11. példa: Házirend-hozzárendelés házirend-eseményeinek lekértése az aktuális előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.

### 12. példa: Házirend-események lekérte egy házirend-hozzárendeléshez a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (a megadott előfizetésben létező) összes erőforráshoz (a bérlő aktuális munkamenet kontextusában) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.

### 13. példa: Házirend-hozzárendelés házirend-eseményeinek lekérte az aktuális előfizetés megadott erőforráscsoportját
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (az előfizetés aktuális munkamenet kontextusában az erőforráscsoportban megtalálható) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendesemény-rekordokat adja vissza.

### 14. példa: Házirendesemények lekérdezése az aktuális előfizetési hatókörben az OrderBy, a Top és a Select lekérdezési beállításokkal
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja. A parancs időbélyeg és házirend-hozzárendelés nevének tulajdonságai alapján rendeli el az eredményeket, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.
Azt is kijelöli, hogy az egyes rekordoszlopok csak egy részkészletét sorolja fel.

### 15. példa: Házirendesemények lekérdezése az aktuális előfizetési hatókörben a From and To lekérdezési beállításokkal
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához megadott dátumtartományon belül létrehozott házirendesemény-rekordokat adja vissza.

### 16. példa: Házirendesemények lekérdezése az aktuális előfizetési hatókörben, a Lekérdezésszűrés lehetőséggel
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja.
A parancs korlátozza a szűrés által visszaadott eredményeket a házirenddefiníciós művelet (beleértve az elutasítási vagy naplózási műveleteket) és az erőforrás helye alapján (a keletus helyet nem foglalja magában).

### 17. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét, és sorszám összesítésének alkalmazása
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordok számát kapja meg.
A parancs csak a házirend eseményrekordjainak számát adja vissza, amelyet az AdditionalProperties tulajdonságban ad vissza.

### 18. példa: Házirendesemények lekértése az aktuális előfizetési hatókörben, csoportosítás alkalmazása összesítéssel
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja. A parancs korlátozza a házirenddefiníciós művelet alapján végzett szűrés által visszaadott eredményeket (csak naplózási és elutasítási eseményeket tartalmaz).
Az eredményeket a házirend-hozzárendelés, a házirend-definíció, a házirenddefiníciós művelet és az erőforrás-azonosító alapján csoportosítja, és kiszámítja az egyes csoportok rekordjainak számát, amelyet az AdditionalProperties tulajdonságban ad vissza.
Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.

### 19. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét, és csoportosítás alkalmazása összesítés nélkül
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja. A parancs korlátozza a házirenddefiníciós művelet alapján végzett szűrés által visszaadott eredményeket (csak naplózási és elutasítási eseményeket tartalmaz).
Az eredményeket az erőforrás-azonosító alapján csoportosulja. Ez a szolgáltatás létrehozza az előfizetés azon erőforrásainak listáját, amelyek legalább egy naplózási vagy elutasítási házirendhez létrehoznak egy házirendeseményt.

### 20. példa: Házirendesemények lekérte az aktuális előfizetés hatókörét, és az Alkalmaz beállítással több csoportosítást adott meg
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához az utolsó napon létrehozott házirendesemény-rekordokat kapja. A parancs korlátozza a szűrés által visszaadott eredményeket a házirend-definíciós művelet alapján (csak elutasítási eseményeket tartalmaz).
Az eredményeket először a házirend-hozzárendelés, a házirend-definíció és az erőforrás-azonosító alapján csoportosulja. Ezután a csoportosítás eredményét az erőforrás-azonosító kivételével ugyanazokkal a tulajdonságokkal csoportosítja, és kiszámítja az egyes csoportok rekordjainak számát, amelyet az AdditionalProperties tulajdonságban ad vissza.
Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.
Ez a legfelső 5 elutasító házirendet hozza létre, amelyekben a legtöbb elutasított erőforrás található.

## PARAMETERS

### -Apply
Kifejezés alkalmazása aggregációkhoz OData-notation használatával.

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

### -Filter
Filter expression using OData notation.

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
ISO 8601 formázott időbélyeg, amely a lekérdezési időköz kezdő idejét adja meg.
Ha nincs megadva, az alapértelmezett érték a "To" paraméter értéke mínusz 1 nap.

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
Felügyeleti csoport neve.

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
Ordering expression using OData notation.
Egy vagy több vesszővel elválasztott oszlopnév opcionális "desc" (alapértelmezett) vagy "asc" értékekkel.

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
Házirend-hozzárendelés neve.

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
Házirenddefiníció neve.

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
Házirendkészlet definíciójának neve.

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
Erőforráscsoport neve.

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
Select expression using OData notation.
Egy vagy több vesszővel elválasztott oszlopnév.
Az egyes rekordokat csak a kért oszlopokra korlátozza.

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
Előfizetés azonosítója.

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
ISO 8601 formázott időbélyeg, amely megadja a lekérdezési időköz záró idejét.
Ha nincs megadva, a kérések alapértelmezett ideje.

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
A vissza nem térhet rekordok maximális száma.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
