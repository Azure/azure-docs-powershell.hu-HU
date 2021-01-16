---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466296"
---
# <span data-ttu-id="dafdc-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="dafdc-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="dafdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dafdc-102">SYNOPSIS</span></span>
<span data-ttu-id="dafdc-103">Frissítse a megoldás címkéit.</span><span class="sxs-lookup"><span data-stu-id="dafdc-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="dafdc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dafdc-104">SYNTAX</span></span>

### <span data-ttu-id="dafdc-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dafdc-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dafdc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dafdc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dafdc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dafdc-107">DESCRIPTION</span></span>
<span data-ttu-id="dafdc-108">Frissítse a megoldás címkéit.</span><span class="sxs-lookup"><span data-stu-id="dafdc-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="dafdc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dafdc-109">EXAMPLES</span></span>

### <span data-ttu-id="dafdc-110">1. példa: Figyelt naplóelemzési megoldás frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="dafdc-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="dafdc-111">Ez a parancs név szerint frissíti a figyelésnapló-elemzési megoldást.</span><span class="sxs-lookup"><span data-stu-id="dafdc-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="dafdc-112">2. példa: Monitornapló-elemzési megoldás frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="dafdc-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="dafdc-113">Ez a parancs objektumról objektumra frissíti a figyelésnapló-elemzési megoldást.</span><span class="sxs-lookup"><span data-stu-id="dafdc-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="dafdc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dafdc-114">PARAMETERS</span></span>

### <span data-ttu-id="dafdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafdc-115">-DefaultProfile</span></span>
<span data-ttu-id="dafdc-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dafdc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dafdc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dafdc-117">-InputObject</span></span>
<span data-ttu-id="dafdc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dafdc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dafdc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dafdc-119">-Name</span></span>
<span data-ttu-id="dafdc-120">Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="dafdc-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dafdc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dafdc-121">-ResourceGroupName</span></span>
<span data-ttu-id="dafdc-122">A lekért erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dafdc-122">The name of the resource group to get.</span></span>
<span data-ttu-id="dafdc-123">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="dafdc-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dafdc-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dafdc-124">-SubscriptionId</span></span>
<span data-ttu-id="dafdc-125">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="dafdc-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dafdc-126">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="dafdc-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dafdc-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="dafdc-127">-Tag</span></span>
<span data-ttu-id="dafdc-128">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="dafdc-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dafdc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dafdc-129">-Confirm</span></span>
<span data-ttu-id="dafdc-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dafdc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dafdc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dafdc-131">-WhatIf</span></span>
<span data-ttu-id="dafdc-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dafdc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dafdc-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dafdc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dafdc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafdc-134">CommonParameters</span></span>
<span data-ttu-id="dafdc-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dafdc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafdc-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dafdc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafdc-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dafdc-137">INPUTS</span></span>

### <span data-ttu-id="dafdc-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="dafdc-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="dafdc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafdc-139">OUTPUTS</span></span>

### <span data-ttu-id="dafdc-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="dafdc-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="dafdc-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dafdc-141">NOTES</span></span>

<span data-ttu-id="dafdc-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dafdc-142">ALIASES</span></span>

<span data-ttu-id="dafdc-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="dafdc-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dafdc-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="dafdc-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dafdc-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dafdc-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dafdc-146">INPUTOBJECT: <IMonitoringSolutionsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="dafdc-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dafdc-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="dafdc-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dafdc-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="dafdc-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="dafdc-149">`[ManagementConfigurationName <String>]`: Felhasználókezelési konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="dafdc-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="dafdc-150">`[ProviderName <String>]`: A szülőerőforrás szolgáltatójának neve.</span><span class="sxs-lookup"><span data-stu-id="dafdc-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="dafdc-151">`[ResourceGroupName <String>]`: A lekért erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dafdc-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="dafdc-152">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="dafdc-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="dafdc-153">`[ResourceName <String>]`: Szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="dafdc-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="dafdc-154">`[ResourceType <String>]`: A szülőerőforrás erőforrástípusa</span><span class="sxs-lookup"><span data-stu-id="dafdc-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="dafdc-155">`[SolutionName <String>]`: Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="dafdc-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="dafdc-156">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="dafdc-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dafdc-157">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="dafdc-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dafdc-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dafdc-158">RELATED LINKS</span></span>

