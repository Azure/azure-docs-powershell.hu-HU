---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154570"
---
# <span data-ttu-id="45296-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="45296-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="45296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45296-102">SYNOPSIS</span></span>
<span data-ttu-id="45296-103">Törli a megoldást az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="45296-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="45296-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="45296-104">SYNTAX</span></span>

### <span data-ttu-id="45296-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45296-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="45296-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45296-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45296-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="45296-107">DESCRIPTION</span></span>
<span data-ttu-id="45296-108">Törli a megoldást az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="45296-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="45296-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="45296-109">EXAMPLES</span></span>

### <span data-ttu-id="45296-110">1. példa: Monitornapló-elemzési megoldás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="45296-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="45296-111">Ez a parancs név szerint eltávolítja a figyelésnapló-elemzési megoldást.</span><span class="sxs-lookup"><span data-stu-id="45296-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="45296-112">2. példa: Monitornapló-elemzési megoldás eltávolítása objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="45296-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="45296-113">Ez a parancs objektumról objektumra eltávolítja a monitornapló-elemzési megoldást.</span><span class="sxs-lookup"><span data-stu-id="45296-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="45296-114">3. példa: Monitornapló-elemzési megoldás eltávolítása folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="45296-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="45296-115">Ez a parancs folyamat szerint eltávolítja a figyelt naplóelemzési megoldást.</span><span class="sxs-lookup"><span data-stu-id="45296-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="45296-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45296-116">PARAMETERS</span></span>

### <span data-ttu-id="45296-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45296-117">-DefaultProfile</span></span>
<span data-ttu-id="45296-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45296-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45296-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45296-119">-InputObject</span></span>
<span data-ttu-id="45296-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="45296-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45296-121">-Name</span><span class="sxs-lookup"><span data-stu-id="45296-121">-Name</span></span>
<span data-ttu-id="45296-122">Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="45296-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45296-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45296-123">-PassThru</span></span>
<span data-ttu-id="45296-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="45296-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="45296-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45296-125">-ResourceGroupName</span></span>
<span data-ttu-id="45296-126">A lekért erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="45296-126">The name of the resource group to get.</span></span>
<span data-ttu-id="45296-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="45296-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45296-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45296-128">-SubscriptionId</span></span>
<span data-ttu-id="45296-129">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="45296-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="45296-130">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="45296-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45296-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45296-131">-Confirm</span></span>
<span data-ttu-id="45296-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="45296-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45296-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45296-133">-WhatIf</span></span>
<span data-ttu-id="45296-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="45296-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45296-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45296-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45296-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45296-136">CommonParameters</span></span>
<span data-ttu-id="45296-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45296-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45296-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45296-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45296-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45296-139">INPUTS</span></span>

### <span data-ttu-id="45296-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="45296-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="45296-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45296-141">OUTPUTS</span></span>

### <span data-ttu-id="45296-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45296-142">System.Boolean</span></span>

## <span data-ttu-id="45296-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="45296-143">NOTES</span></span>

<span data-ttu-id="45296-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="45296-144">ALIASES</span></span>

<span data-ttu-id="45296-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="45296-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45296-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="45296-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45296-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45296-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45296-148">INPUTOBJECT: <IMonitoringSolutionsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="45296-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45296-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="45296-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45296-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="45296-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="45296-151">`[ManagementConfigurationName <String>]`: Felhasználókezelési konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="45296-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="45296-152">`[ProviderName <String>]`: A szülőerőforrás szolgáltatójának neve.</span><span class="sxs-lookup"><span data-stu-id="45296-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="45296-153">`[ResourceGroupName <String>]`: A lekért erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="45296-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="45296-154">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="45296-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="45296-155">`[ResourceName <String>]`: Szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="45296-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="45296-156">`[ResourceType <String>]`: A szülőerőforrás erőforrástípusa</span><span class="sxs-lookup"><span data-stu-id="45296-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="45296-157">`[SolutionName <String>]`: Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="45296-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="45296-158">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="45296-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="45296-159">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="45296-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="45296-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45296-160">RELATED LINKS</span></span>

