---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 2ce25f0881fff9ee684bcf234d13d847b7f28850
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361995"
---
# <span data-ttu-id="8cb11-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8cb11-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="8cb11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cb11-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb11-103">Létrehoz egy újat, vagy beállítja egy meglévő tevékenységnapló-riasztást.</span><span class="sxs-lookup"><span data-stu-id="8cb11-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="8cb11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8cb11-104">SYNTAX</span></span>

### <span data-ttu-id="8cb11-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cb11-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb11-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cb11-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb11-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8cb11-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cb11-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8cb11-108">DESCRIPTION</span></span>
<span data-ttu-id="8cb11-109">A **Set-AzActivityLogAlert** parancsmag létrehoz egy újat, vagy beállít egy meglévő tevékenységnapló-riasztást.</span><span class="sxs-lookup"><span data-stu-id="8cb11-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="8cb11-110">Címkék, feltételek és műveletek esetén az objektumokat előre létre kell hoznunk, és paraméterekként kell átesni a hívásban vesszővel elválasztva (lásd az alábbi példát).</span><span class="sxs-lookup"><span data-stu-id="8cb11-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="8cb11-111">Ez a parancsmag implementálja a ShouldProcess mintát, azaz az erőforrás létrehozása/módosítása előtt megerősítést kérhet a felhasználótól.</span><span class="sxs-lookup"><span data-stu-id="8cb11-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="8cb11-112">**MEGJEGYZÉS:** Ez a parancsmag és a hozzá kapcsolódó parancsmag felváltja az elavult (2017. novemberi) **Add-AzLogAlertRule bővítményt.**</span><span class="sxs-lookup"><span data-stu-id="8cb11-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="8cb11-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8cb11-113">EXAMPLES</span></span>

### <span data-ttu-id="8cb11-114">1. példa: Tevékenységnapló-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cb11-114">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="8cb11-115">Az első négy parancs levél feltételt és műveletcsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cb11-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="8cb11-116">Az utolsó parancs egy tevékenységnapló-riasztást hoz létre a feltétel és a műveletcsoport használatával.</span><span class="sxs-lookup"><span data-stu-id="8cb11-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="8cb11-117">2. példa: Letiltott tevékenységnapló-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cb11-117">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="8cb11-118">Az első négy parancs levél feltételt és műveletcsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cb11-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="8cb11-119">Az utolsó parancs létrehoz egy tevékenységnapló-riasztást a feltétel és a műveletcsoport használatával, de letiltja a riasztást.</span><span class="sxs-lookup"><span data-stu-id="8cb11-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="8cb11-120">3. példa: Tevékenységnapló-riasztás beállítása a pipa vagy az InputObject paraméter értéke alapján</span><span class="sxs-lookup"><span data-stu-id="8cb11-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="8cb11-121">Az első parancs a nop-hoz hasonlóan beállítja a riasztást ugyanazokkal az értékekkel, amelyek már tartalmazták a többi parancsot is, lekéri a riasztási szabályt, módosítja és letiltja a leírást, majd az InputObject paraméter használatával megőrzi ezeket a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="8cb11-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="8cb11-122">4. példa: Tevékenységnapló-riasztás beállítása a pipa ResourceId értéke alapján</span><span class="sxs-lookup"><span data-stu-id="8cb11-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="8cb11-123">Ha a megadott naplóriasztás szabály létezik, ez a parancs letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="8cb11-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="8cb11-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cb11-124">PARAMETERS</span></span>

### <span data-ttu-id="8cb11-125">-Művelet</span><span class="sxs-lookup"><span data-stu-id="8cb11-125">-Action</span></span>
<span data-ttu-id="8cb11-126">A tevékenységnapló-riasztáshoz szükséges műveletcsoportok listája.</span><span class="sxs-lookup"><span data-stu-id="8cb11-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="8cb11-127">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="8cb11-127">-Condition</span></span>
<span data-ttu-id="8cb11-128">A tevékenységnapló-riasztás feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="8cb11-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="8cb11-129">**MEGJEGYZÉS:** A feltételek listájában legalább egynek "Kategória" értékű mezőnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8cb11-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="8cb11-130">A backend válaszol a 400 (BadRequest) feltétellel, ha ez a feltétel nem áll be.</span><span class="sxs-lookup"><span data-stu-id="8cb11-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="8cb11-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb11-131">-DefaultProfile</span></span>
<span data-ttu-id="8cb11-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8cb11-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cb11-133">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8cb11-133">-Description</span></span>
<span data-ttu-id="8cb11-134">A riasztási erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="8cb11-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="8cb11-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="8cb11-135">-DisableAlert</span></span>
<span data-ttu-id="8cb11-136">Lehetővé teszi, hogy a felhasználó letiltott tevékenységnapló-riasztást hozzon létre.</span><span class="sxs-lookup"><span data-stu-id="8cb11-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="8cb11-137">Ha nincs megadva, a riasztások engedélyezve vannak.</span><span class="sxs-lookup"><span data-stu-id="8cb11-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="8cb11-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cb11-138">-InputObject</span></span>
<span data-ttu-id="8cb11-139">Beállítja a hívás InputObject tags tulajdonságát a szükséges név és az erőforráscsoport nevének tulajdonságainak kibontása érdekében.</span><span class="sxs-lookup"><span data-stu-id="8cb11-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="8cb11-140">-Location</span><span class="sxs-lookup"><span data-stu-id="8cb11-140">-Location</span></span>
<span data-ttu-id="8cb11-141">Az a hely, ahol a tevékenységnapló-riasztás létezik.</span><span class="sxs-lookup"><span data-stu-id="8cb11-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="8cb11-142">-Name</span><span class="sxs-lookup"><span data-stu-id="8cb11-142">-Name</span></span>
<span data-ttu-id="8cb11-143">A tevékenységnapló-riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="8cb11-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="8cb11-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb11-144">-ResourceGroupName</span></span>
<span data-ttu-id="8cb11-145">Annak az erőforráscsoportnak a neve, amelyben a riasztási erőforrás fog létezni.</span><span class="sxs-lookup"><span data-stu-id="8cb11-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="8cb11-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cb11-146">-ResourceId</span></span>
<span data-ttu-id="8cb11-147">Beállítja a hívás ResourceId tags tulajdonságát a szükséges név, az erőforráscsoport nevének tulajdonságainak kibontása érdekében.</span><span class="sxs-lookup"><span data-stu-id="8cb11-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="8cb11-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="8cb11-148">-Scope</span></span>
<span data-ttu-id="8cb11-149">A tevékenységnapló-riasztás hatókörének listája.</span><span class="sxs-lookup"><span data-stu-id="8cb11-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="8cb11-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="8cb11-150">-Tag</span></span>
<span data-ttu-id="8cb11-151">Beállítja a tevékenységnapló riasztási erőforrásának címketulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="8cb11-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="8cb11-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cb11-152">-Confirm</span></span>
<span data-ttu-id="8cb11-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8cb11-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cb11-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb11-154">-WhatIf</span></span>
<span data-ttu-id="8cb11-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8cb11-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cb11-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cb11-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cb11-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb11-157">CommonParameters</span></span>
<span data-ttu-id="8cb11-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb11-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb11-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cb11-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb11-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8cb11-160">INPUTS</span></span>

### <span data-ttu-id="8cb11-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8cb11-161">System.String</span></span>

### <span data-ttu-id="8cb11-162">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8cb11-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8cb11-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8cb11-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8cb11-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8cb11-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8cb11-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8cb11-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8cb11-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8cb11-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8cb11-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cb11-167">OUTPUTS</span></span>

### <span data-ttu-id="8cb11-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8cb11-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8cb11-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8cb11-169">NOTES</span></span>

## <span data-ttu-id="8cb11-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cb11-170">RELATED LINKS</span></span>

[<span data-ttu-id="8cb11-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8cb11-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="8cb11-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8cb11-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="8cb11-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8cb11-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="8cb11-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8cb11-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="8cb11-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8cb11-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="8cb11-176">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="8cb11-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
