---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206271"
---
# Get-AzPolicyState

## SYNOPSIS
Házirend-megfelelőségi államokat biztosít az erőforrásokhoz.

## SZINTAXIS

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

### ResourceScope
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

## LEÍRÁS
Házirend-megfelelőségi államokat biztosít az erőforrásokhoz. A házirendállapot-rekordok lekérdezhetők különböző hatókörökben. A megadott időintervallum alapján (alapértelmezés szerint az utolsó nap) lekérdezhető a legújabb házirendállapotok vagy az összes házirendállapot-áttűnés. Az eredmények szűrhetők, csoportosíthatóak és csoportos összesítések is kiszámíthatók.

## PÉLDÁK

### 1. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét
```powershell
PS C:\> Get-AzPolicyState
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.

### 2. példa: A legújabb házirend-államok lekérte a megadott előfizetési hatókört
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

A megadott előfizetésen belüli összes erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 3. példa: Az előfizetés aktuális hatókörében lévő házirend-állapotok lekérte
```powershell
PS C:\> Get-AzPolicyState -All
```

Az aktuális munkamenet kontextusában az előfizetésben lévő összes erőforrásra vonatkozóan az utolsó napon létrehozott összes előzmény-házirendállapot-rekordot (beleértve a legutóbbi rekordokat is) beveszi.

### 4. példa: A legújabb házirend-államok lekérte a felügyeleti csoportok hatókörét
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

A megadott felügyeleti csoporton belüli összes erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 5. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés erőforráscsoport-hatókörét
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoport összes erőforrásához (az aktuális munkamenet kontextusában az előfizetésben) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 6. példa: A legújabb házirend-államok lekérte az erőforráscsoport hatókörét a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoport összes erőforrásához (a megadott előfizetésben) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 7. példa: Erőforrás legújabb házirend- states-ának lekérte
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

A megadott erőforrás utolsó napján létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 8. példa: Házirendkészlet-definíció legújabb házirend-állapotának lekérte az aktuális előfizetésben
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirendkészlet-definíció által (az aktuális munkamenet kontextusában az előfizetésben megtalálható) összes erőforrásra vonatkozóan (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.

### 9. példa: Házirendkészlet-definíció legújabb házirend-államok lekérte a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirendkészlet-definíció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza (a bérlői webhelyen az aktuális munkamenet kontextusában).

### 10. példa: Házirenddefiníció legújabb házirend-állapotának lekérte az aktuális előfizetésben
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirenddefiníció által (az aktuális munkamenet kontextusában az előfizetésben megtalálható) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.

### 11. példa: Házirenddefiníció legújabb házirend-államának lekérte a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirenddefiníció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza (a bérlői webhelyen az aktuális munkamenet kontextusában).

### 12. példa: Házirend-hozzárendelés legújabb házirend-állapotának lekérte az aktuális előfizetésben
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetésben létezik) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott házirendállapot-rekordokat adja vissza.

### 13. példa: Házirend-hozzárendelés legújabb házirend-kiosztási államának lekérte a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott (a megadott előfizetésben létező) házirend-hozzárendelés által az utolsó napon létrehozott összes erőforrásra vonatkozóan (a bérlő aktuális munkamenet kontextusában) létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 14. példa: Házirend-hozzárendelés legújabb házirend-állapotának lekérte az aktuális előfizetés megadott erőforráscsoportját
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (az előfizetés aktuális munkamenet kontextusában az erőforráscsoportban található) összes erőforráshoz (a jelenlegi munkamenet kontextusában a bérlőn belül) az utolsó napon létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 15. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetési hatókört az OrderBy, a Top és a Select lekérdezési beállításokkal
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le. A parancs időbélyeg és házirend-hozzárendelés nevének tulajdonságai alapján rendeli el az eredményeket, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.
Azt is kijelöli, hogy az egyes rekordoszlopok csak egy részkészletét sorolja fel.

### 16. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét, a From and To lekérdezési beállításokkal
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához megadott dátumtartományon belül létrehozott legújabb házirendállapot-rekordokat adja vissza.

### 17. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét a Szűrés lekérdezési beállítással
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le.
A parancs korlátozza a szűrés által visszaadott eredményeket a házirenddefiníciós művelet (beleértve az elutasítási vagy naplózási műveleteket), a megfelelőségi állapot (csak a nem megfelelő állapotot is beleértve) és az erőforrás helye alapján (a kelettől függetlenül).

### 18. példa: A legújabb házirendállapotok lekértése az aktuális előfizetés hatókörében a sorszám összesítésének alkalmazásával
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Az aktuális munkamenet kontextusában az előfizetésben lévő összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordok számát kapja meg.
A parancs csak a házirendállapot-rekordok számát adja vissza, amelyet az AdditionalProperties tulajdonságban ad vissza.

### 19. példa: A legújabb házirendállapotok lekértése az aktuális előfizetési hatókörben a Csoportosítás alkalmazása aggregációval beállítással
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le. A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).
Az eredményeket a házirend-hozzárendelés, a házirendkészlet-definíció és a házirend-definíció alapján csoportosítja, és az egyes csoportok rekordjainak számát számítja ki, amelyet az AdditionalProperties tulajdonságban ad vissza.
Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.

### 20. példa: A legújabb házirendállapotok lekértése az aktuális előfizetési hatókörben a Csoportosítás alkalmazása összesítés nélkül beállítással
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le. A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).
Az eredményeket az erőforrás-azonosító alapján csoportosulja. Ez a szolgáltatás létrehozza az előfizetés azon erőforrásainak listáját, amelyek nem kompatibilisek legalább egy házirendnek.

### 21. példa: A legújabb házirend-állapotok lekérte az aktuális előfizetés hatókörét, és több csoportosítást is megadhat az Alkalmazás beállítással
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### 22. példa: Az erőforrás legújabb házirend-ének megtekintése, beleértve a házirendek kiértékelési részleteit
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirendállapot-rekordokat kapja le. A parancs korlátozza a megfelelőségi állapot alapján való szűrés által visszaadott eredményeket (csak a nem megfelelő állapotot tartalmazza).
Az eredményeket először a házirend-hozzárendelés, a házirend-definíció, a házirend-definíció és az erőforrás-azonosító alapján csoportosulja. Ezután a csoportosítás eredményét az erőforrás-azonosító kivételével ugyanazokkal a tulajdonságokkal csoportosítja, és kiszámítja az egyes csoportok rekordjainak számát, amelyet az AdditionalProperties tulajdonságban ad vissza.
Az eredményeket a számlálás összesítése szerint csökkenő sorrendbe rendezi, és az ebben a sorrendben felsoroltak közül csak a 5-öt veszi fel.
Ez a legfelső 5 házirendet hozza létre, amelyekben a legtöbb nem kompatibilis erőforrás található.

## PARAMETERS

### -All
A megadott időintervallumon belül csak a legújabb házirendek helyett az összes házirend-államot be kell szereznie.

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

### -Kibontás
Kifejezés kibontása OData-notation használatával

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

### -Filter
Kifejezésszűrés OData-ként

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
ISO 8601 formázott időbélyeg, amely megadja a lekérdezési időköz kezdő idejét.
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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
