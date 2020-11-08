---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 2ce25f0881fff9ee684bcf234d13d847b7f28850
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018183"
---
# <span data-ttu-id="da374-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da374-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="da374-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da374-102">SYNOPSIS</span></span>
<span data-ttu-id="da374-103">Új vagy meglévő tevékenység-naplózási riasztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da374-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="da374-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da374-104">SYNTAX</span></span>

### <span data-ttu-id="da374-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="da374-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da374-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da374-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da374-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="da374-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da374-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="da374-108">DESCRIPTION</span></span>
<span data-ttu-id="da374-109">A **set-AzActivityLogAlert** parancsmag új vagy meglévő tevékenység-naplózási riasztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da374-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="da374-110">Címkék, feltételek és műveletek esetén az objektumokat előre kell létrehozni, és a hívásban paraméterként kell átadni, mint vesszővel elválasztva (lásd az alábbi példát).</span><span class="sxs-lookup"><span data-stu-id="da374-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="da374-111">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása/módosítása előtt.</span><span class="sxs-lookup"><span data-stu-id="da374-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="da374-112">**Megjegyzés** : Ez a parancsmag és a hozzá kapcsolódóak a megszűnt (november 2017) **bővítményt** cserélik le a AzLogAlertRule.</span><span class="sxs-lookup"><span data-stu-id="da374-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="da374-113">Példák</span><span class="sxs-lookup"><span data-stu-id="da374-113">EXAMPLES</span></span>

### <span data-ttu-id="da374-114">1. példa: műveletnapló-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="da374-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="da374-115">Az első négy parancs a levél feltételeit és a műveletek csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="da374-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="da374-116">A végleges parancs a feltétel és a művelet csoporttal hoz létre egy tevékenység-naplózási riasztást.</span><span class="sxs-lookup"><span data-stu-id="da374-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="da374-117">2. példa: tevékenység naplójának létrehozása letiltva</span><span class="sxs-lookup"><span data-stu-id="da374-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="da374-118">Az első négy parancs a levél feltételeit és a műveletek csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="da374-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="da374-119">A végleges parancs tevékenység-naplózási értesítést hoz létre a feltétel és a művelet csoport segítségével, de a riasztást letiltja.</span><span class="sxs-lookup"><span data-stu-id="da374-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="da374-120">3. példa: műveletnapló beállítása a pipe vagy a InputObject paraméter értéke alapján</span><span class="sxs-lookup"><span data-stu-id="da374-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="da374-121">Az első parancs hasonlít egy NOP, a riasztást ugyanazokkal az értékekkel adja meg, amelyekben már megtalálható a többi parancs a riasztási szabály lekérése után, megváltoztathatja a leírást, és letilthatja, majd a InputObject paraméterrel megmaradhatja ezeket a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="da374-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="da374-122">4. példa: műveletnapló beállítása a ResourceId érték alapján a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="da374-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="da374-123">Ha az adott naplózási riasztási szabály létezik: Ez a parancs letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="da374-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="da374-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da374-124">PARAMETERS</span></span>

### <span data-ttu-id="da374-125">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="da374-125">-Action</span></span>
<span data-ttu-id="da374-126">A műveletnapló riasztási csoportjának listája.</span><span class="sxs-lookup"><span data-stu-id="da374-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-127">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="da374-127">-Condition</span></span>
<span data-ttu-id="da374-128">A tevékenység naplójának riasztási feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="da374-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="da374-129">**Megjegyzés** : a feltételek listájában legalább egy olyan mezőnek kell lennie, amely egyenlő "Category"-val.</span><span class="sxs-lookup"><span data-stu-id="da374-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="da374-130">Ha ez a feltétel nem jelenik meg, a backend válaszol a 400 (BadRequest) értékre.</span><span class="sxs-lookup"><span data-stu-id="da374-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da374-131">-DefaultProfile</span></span>
<span data-ttu-id="da374-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="da374-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da374-133">-Leírás</span><span class="sxs-lookup"><span data-stu-id="da374-133">-Description</span></span>
<span data-ttu-id="da374-134">Az értesítési erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="da374-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="da374-135">-DisableAlert</span></span>
<span data-ttu-id="da374-136">Lehetővé teszi, hogy a felhasználó letiltotta a tevékenység naplójának riasztását.</span><span class="sxs-lookup"><span data-stu-id="da374-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="da374-137">Ha nem adja meg, akkor a rendszer engedélyezi a riasztások létrehozását.</span><span class="sxs-lookup"><span data-stu-id="da374-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da374-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da374-138">-InputObject</span></span>
<span data-ttu-id="da374-139">A hívás InputObject (címkék) tulajdonságát adja meg a szükséges név és az erőforrás csoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="da374-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-140">-Hely</span><span class="sxs-lookup"><span data-stu-id="da374-140">-Location</span></span>
<span data-ttu-id="da374-141">Az a hely, ahol a műveletnapló figyelmeztetése megtalálható.</span><span class="sxs-lookup"><span data-stu-id="da374-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da374-142">-Name</span></span>
<span data-ttu-id="da374-143">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="da374-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da374-144">-ResourceGroupName</span></span>
<span data-ttu-id="da374-145">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="da374-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da374-146">-ResourceId</span></span>
<span data-ttu-id="da374-147">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="da374-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-148">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="da374-148">-Scope</span></span>
<span data-ttu-id="da374-149">A tevékenység naplójának riasztására vonatkozó hatókörök listája.</span><span class="sxs-lookup"><span data-stu-id="da374-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="da374-150">-Tag</span></span>
<span data-ttu-id="da374-151">A tevékenység naplója riasztási erőforrás címkék tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="da374-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da374-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da374-152">-Confirm</span></span>
<span data-ttu-id="da374-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da374-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da374-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da374-154">-WhatIf</span></span>
<span data-ttu-id="da374-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da374-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da374-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da374-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da374-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da374-157">CommonParameters</span></span>
<span data-ttu-id="da374-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da374-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da374-159">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da374-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da374-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da374-160">INPUTS</span></span>

### <span data-ttu-id="da374-161">System. String</span><span class="sxs-lookup"><span data-stu-id="da374-161">System.String</span></span>

### <span data-ttu-id="da374-162">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="da374-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="da374-163">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertLeafCondition, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="da374-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="da374-164">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertActionGroup, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="da374-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="da374-165">System. Collections. Generic. Dictionary ' 2 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e], [System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="da374-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="da374-166">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="da374-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="da374-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da374-167">OUTPUTS</span></span>

### <span data-ttu-id="da374-168">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="da374-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="da374-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da374-169">NOTES</span></span>

## <span data-ttu-id="da374-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da374-170">RELATED LINKS</span></span>

[<span data-ttu-id="da374-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da374-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="da374-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da374-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="da374-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da374-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="da374-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="da374-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="da374-175">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="da374-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="da374-176">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="da374-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
