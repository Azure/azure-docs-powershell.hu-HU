---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679078"
---
# <span data-ttu-id="17e5a-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="17e5a-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="17e5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="17e5a-103">Új vagy meglévő tevékenység-naplózási riasztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="17e5a-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17e5a-104">SYNTAX</span></span>

### <span data-ttu-id="17e5a-105">A műveletnapló riasztásának beállítása alapértelmezett paraméterei</span><span class="sxs-lookup"><span data-stu-id="17e5a-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e5a-106">A ResourceId a pipe-ról történő átvételét jelző paraméterek</span><span class="sxs-lookup"><span data-stu-id="17e5a-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e5a-107">A tevékenység-naplózási riasztások értékének beállítására szolgáló paraméterek a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="17e5a-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17e5a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="17e5a-108">DESCRIPTION</span></span>
<span data-ttu-id="17e5a-109">A **set-AzureRmActivityLogAlert** parancsmag új vagy meglévő tevékenység-naplózási riasztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="17e5a-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="17e5a-110">Címkék, feltételek és műveletek esetén az objektumokat előre kell létrehozni, és a hívásban paraméterként kell átadni, mint vesszővel elválasztva (lásd az alábbi példát).</span><span class="sxs-lookup"><span data-stu-id="17e5a-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="17e5a-111">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása/módosítása előtt.</span><span class="sxs-lookup"><span data-stu-id="17e5a-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="17e5a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="17e5a-112">EXAMPLES</span></span>

### <span data-ttu-id="17e5a-113">1. példa: műveletnapló-értesítés létrehozása</span><span class="sxs-lookup"><span data-stu-id="17e5a-113">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="17e5a-114">Az első négy parancs a levél feltételeit és a műveletek csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="17e5a-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="17e5a-115">A végleges parancs a feltétel és a művelet csoporttal hoz létre egy tevékenység-naplózási riasztást.</span><span class="sxs-lookup"><span data-stu-id="17e5a-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="17e5a-116">2. példa: tevékenység naplójának létrehozása letiltva</span><span class="sxs-lookup"><span data-stu-id="17e5a-116">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="17e5a-117">Az első négy parancs a levél feltételeit és a műveletek csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="17e5a-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="17e5a-118">A végleges parancs tevékenység-naplózási értesítést hoz létre a feltétel és a művelet csoport segítségével, de a riasztást letiltja.</span><span class="sxs-lookup"><span data-stu-id="17e5a-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="17e5a-119">3. példa: műveletnapló beállítása a pipe vagy a InputObject paraméter értéke alapján</span><span class="sxs-lookup"><span data-stu-id="17e5a-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="17e5a-120">Az első parancs hasonlít egy NOP, a riasztást ugyanazokkal az értékekkel adja meg, amelyekben már megtalálható a többi parancs a riasztási szabály lekérése után, megváltoztathatja a leírást, és letilthatja, majd a InputObject paraméterrel megmaradhatja ezeket a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="17e5a-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="17e5a-121">4. példa: műveletnapló beállítása a ResourceId érték alapján a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="17e5a-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="17e5a-122">Ha az adott naplózási riasztási szabály létezik: Ez a parancs letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="17e5a-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="17e5a-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17e5a-123">PARAMETERS</span></span>

### <span data-ttu-id="17e5a-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="17e5a-124">-Location</span></span>
<span data-ttu-id="17e5a-125">Az a hely, ahol a műveletnapló figyelmeztetése megtalálható.</span><span class="sxs-lookup"><span data-stu-id="17e5a-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17e5a-126">-Name</span></span>
<span data-ttu-id="17e5a-127">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="17e5a-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e5a-128">-ResourceGroupName</span></span>
<span data-ttu-id="17e5a-129">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="17e5a-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-130">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="17e5a-130">-Scope</span></span>
<span data-ttu-id="17e5a-131">A tevékenység naplójának riasztására vonatkozó hatókörök listája.</span><span class="sxs-lookup"><span data-stu-id="17e5a-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-132">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="17e5a-132">-Condition</span></span>
<span data-ttu-id="17e5a-133">A tevékenység naplójának riasztási feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="17e5a-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="17e5a-134">**Megjegyzés** : a feltételek listájában legalább egy olyan mezőnek kell lennie, amely egyenlő "Category"-val.</span><span class="sxs-lookup"><span data-stu-id="17e5a-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="17e5a-135">Ha ez a feltétel nem jelenik meg, a backend válaszol a 400 (BadRequest) értékre.</span><span class="sxs-lookup"><span data-stu-id="17e5a-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-136">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="17e5a-136">-Action</span></span>
<span data-ttu-id="17e5a-137">A műveletnapló riasztási csoportjának listája.</span><span class="sxs-lookup"><span data-stu-id="17e5a-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="17e5a-138">-DisableAlert</span></span>
<span data-ttu-id="17e5a-139">Lehetővé teszi, hogy a felhasználó letiltotta a tevékenység naplójának riasztását.</span><span class="sxs-lookup"><span data-stu-id="17e5a-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="17e5a-140">Ha nem adja meg, akkor a rendszer engedélyezi a riasztások létrehozását.</span><span class="sxs-lookup"><span data-stu-id="17e5a-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-141">-Leírás</span><span class="sxs-lookup"><span data-stu-id="17e5a-141">-Description</span></span>
<span data-ttu-id="17e5a-142">Az értesítési erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="17e5a-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="17e5a-143">-Tag</span></span>
<span data-ttu-id="17e5a-144">A tevékenység naplója riasztási erőforrás címkék tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="17e5a-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17e5a-145">-InputObject</span></span>
<span data-ttu-id="17e5a-146">A hívás InputObject (címkék) tulajdonságát adja meg a szükséges név és az erőforrás csoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="17e5a-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17e5a-147">-ResourceId</span></span>
<span data-ttu-id="17e5a-148">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="17e5a-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17e5a-149">-Confirm</span></span>
<span data-ttu-id="17e5a-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17e5a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e5a-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e5a-151">-DefaultProfile</span></span>
<span data-ttu-id="17e5a-152">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17e5a-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e5a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e5a-153">-WhatIf</span></span>
<span data-ttu-id="17e5a-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17e5a-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17e5a-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17e5a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e5a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e5a-156">CommonParameters</span></span>
<span data-ttu-id="17e5a-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17e5a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e5a-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e5a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e5a-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17e5a-159">INPUTS</span></span>

## <span data-ttu-id="17e5a-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17e5a-160">OUTPUTS</span></span>

### <span data-ttu-id="17e5a-161">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="17e5a-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="17e5a-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17e5a-162">NOTES</span></span>

## <span data-ttu-id="17e5a-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17e5a-163">RELATED LINKS</span></span>

[<span data-ttu-id="17e5a-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="17e5a-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="17e5a-165">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="17e5a-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="17e5a-166">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="17e5a-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="17e5a-167">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="17e5a-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="17e5a-168">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="17e5a-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="17e5a-169">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="17e5a-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
