---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372509"
---
# Get-AzPolicyStateSummary

## SYNOPSIS
Az erőforrásokra vonatkozó legújabb, házirend-megfelelőségi államokra vonatkozó összefoglalást kap.

## SZINTAXIS

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

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Összegző nézetet kap a házirendek megfelelőségi állapotszámairól különböző hatókörökben, házirend-hozzárendelések és házirend-definíciók szerint bontva. Csak a házirendnek nem megfelelő államokat tartalmazza.

## PÉLDÁK

### 1. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja.

### 2. példa: A házirendek legújabb, nem megfelelő államokkal kapcsolatos összesítése a megadott előfizetési hatókörben
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

A megadott előfizetésben található összes erőforrás utolsó napján létrehozott legújabb házirend-megfelelőségi államok összefoglaló nézetét kapja.

### 3. példa: A házirendek legújabb, nem megfelelő államokkal kapcsolatos összegzése a felügyeleti csoportok hatókörében
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

A megadott felügyeleti csoportban található összes erőforrás utolsó napján létrehozott legújabb házirend-megfelelőségi államok összegzési nézete.

### 4. példa: A legújabb, nem megfelelő házirend-állapotok összegzése az aktuális előfizetés erőforráscsoport-hatókörében
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoport összes erőforrásához (az aktuális munkamenet kontextusában) az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja.

### 5. példa: A házirendek legújabb, nem megfelelő államokkal kapcsolatos összegzése a megadott előfizetés erőforráscsoport-hatókörében
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

A megadott erőforráscsoporton belül (a megadott előfizetésben) az utolsó napon létrehozott legújabb házirend-megfelelőségi államok összegzését kapja.

### 6. példa: Az erőforrás legújabb, nem megfelelő házirend-államokra vonatkozó összesítésének lekérte
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

A megadott erőforrás utolsó napján létrehozott legújabb házirend-megfelelőségi államok összegzési nézete.

### 7. példa: Az aktuális előfizetés házirendkészlet-definíciójának legújabb, nem megfelelő házirend-állapotok összesítése
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirendkészlet-definíció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.

### 8. példa: A házirend-definíció legújabb, nem megfelelő házirend-államokra vonatkozó összegzése a megadott előfizetésben
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirendkészlet-definíció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.

### 9. példa: Az aktuális előfizetés házirenddefiníciójának legújabb, nem megfelelő házirend-állapotok összesítése
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirenddefiníció által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.

### 10. példa: A házirendek legújabb, nem megfelelő államokkal kapcsolatos összesítése a megadott előfizetés házirenddefinícióihoz
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

A megadott házirenddefiníció által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.

### 11. példa: Az aktuális előfizetés házirend-hozzárendelésének legújabb, nem megfelelő házirend-állapotok összefoglalása
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzési nézete.

### 12. példa: A házirendek legújabb, nem megfelelő államokra vonatkozó összegzése a megadott előfizetés házirend-hozzárendeléséhez
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (a megadott előfizetésben létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott házirend-megfelelőségi állapotok összegzési nézete.

### 13. példa: Az aktuális előfizetés megadott erőforráscsoportja házirend-hozzárendelésének legújabb, nem megfelelő házirend-állapotok összegzése
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

A megadott házirend-hozzárendelés által (az aktuális munkamenet kontextusában az előfizetés erőforráscsoportban létező) összes erőforrásra vonatkozóan az utolsó napon létrehozott házirend-megfelelőségi állapotok összegzési nézete.

### 14. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben a Felső lekérdezés lehetőséggel
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja. A parancs csökkenő sorrendbe rendezi az eredményekben a házirend-hozzárendelések összegzését úgy, hogy a nem megfelelő erőforrások száma csökkenő sorrendben van, és a házirend-hozzárendelések összefoglalói közül csak az első 5-öt veszi fel.

### 15. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben, a From and To lekérdezési beállításokkal
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrásához megadott dátumtartományon belül létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja.

### 16. példa: A legújabb, nem kompatibilis házirend-állapotok összegzése az aktuális előfizetési hatókörben a Szűrő lekérdezés lehetőséggel
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Az aktuális munkamenet kontextusában az előfizetés összes erőforrására vonatkozóan az utolsó napon létrehozott legújabb házirend-megfelelőségi állapotok összegzését kapja.
A parancs korlátozza a házirenddefiníciós művelet (beleértve az elutasítási vagy naplózási műveleteket) és az erőforrás helye alapján végzett szűrés által visszaadott eredményeket (a független helyeket nem foglalja magában).

## PARAMETERS

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPolicyState](./Get-AzPolicyState.md)
