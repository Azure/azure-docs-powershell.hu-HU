---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154603"
---
# <span data-ttu-id="9816a-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="9816a-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="9816a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9816a-102">SYNOPSIS</span></span>
<span data-ttu-id="9816a-103">Beolvassa a felhasználói megoldást.</span><span class="sxs-lookup"><span data-stu-id="9816a-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="9816a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9816a-104">SYNTAX</span></span>

### <span data-ttu-id="9816a-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9816a-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9816a-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="9816a-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9816a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9816a-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9816a-108">Lista</span><span class="sxs-lookup"><span data-stu-id="9816a-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9816a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9816a-109">DESCRIPTION</span></span>
<span data-ttu-id="9816a-110">Beolvassa a felhasználói megoldást.</span><span class="sxs-lookup"><span data-stu-id="9816a-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="9816a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9816a-111">EXAMPLES</span></span>

### <span data-ttu-id="9816a-112">1. példa: Figyelt naplóelemzési megoldás lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="9816a-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9816a-113">Ez a parancs név alapján naplóelemzési megoldást kap.</span><span class="sxs-lookup"><span data-stu-id="9816a-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="9816a-114">2. példa: Figyelésnapló-elemzési megoldás lekérte erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="9816a-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="9816a-115">Ez a parancs erőforrásazonosítók szerint figyelt naplóelemzési megoldást kap.</span><span class="sxs-lookup"><span data-stu-id="9816a-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="9816a-116">3. példa: Monitornapló-elemzési megoldás lekérte objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="9816a-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9816a-117">Ez a parancs objektumról-objektumra kapja a figyelésnapló-elemzési megoldást.</span><span class="sxs-lookup"><span data-stu-id="9816a-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="9816a-118">4. példa: Az összes figyelésnapló-elemzési megoldás lekérte egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="9816a-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9816a-119">Ez a parancs egy erőforráscsoport összes naplóelemzési megoldását beveszi.</span><span class="sxs-lookup"><span data-stu-id="9816a-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="9816a-120">5. példa: Az összes figyelésnapló-elemzési megoldás lekérte egy előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="9816a-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9816a-121">Ez a parancs az összes figyelésnapló-elemzési megoldást lekérte egy előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="9816a-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="9816a-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9816a-122">PARAMETERS</span></span>

### <span data-ttu-id="9816a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9816a-123">-DefaultProfile</span></span>
<span data-ttu-id="9816a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9816a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9816a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9816a-125">-InputObject</span></span>
<span data-ttu-id="9816a-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9816a-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9816a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9816a-127">-Name</span></span>
<span data-ttu-id="9816a-128">Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="9816a-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9816a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9816a-129">-ResourceGroupName</span></span>
<span data-ttu-id="9816a-130">A lekért erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9816a-130">The name of the resource group to get.</span></span>
<span data-ttu-id="9816a-131">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9816a-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9816a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9816a-132">-SubscriptionId</span></span>
<span data-ttu-id="9816a-133">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9816a-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9816a-134">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9816a-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9816a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9816a-135">CommonParameters</span></span>
<span data-ttu-id="9816a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9816a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9816a-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9816a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9816a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9816a-138">INPUTS</span></span>

### <span data-ttu-id="9816a-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="9816a-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="9816a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9816a-140">OUTPUTS</span></span>

### <span data-ttu-id="9816a-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="9816a-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="9816a-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9816a-142">NOTES</span></span>

<span data-ttu-id="9816a-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9816a-143">ALIASES</span></span>

<span data-ttu-id="9816a-144">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9816a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9816a-145">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9816a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9816a-146">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9816a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9816a-147">INPUTOBJECT: <IMonitoringSolutionsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9816a-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9816a-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9816a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9816a-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="9816a-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="9816a-150">`[ManagementConfigurationName <String>]`: Felhasználókezelési konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="9816a-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="9816a-151">`[ProviderName <String>]`: A szülőerőforrás szolgáltatójának neve.</span><span class="sxs-lookup"><span data-stu-id="9816a-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="9816a-152">`[ResourceGroupName <String>]`: A lekért erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9816a-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="9816a-153">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9816a-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="9816a-154">`[ResourceName <String>]`: Szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="9816a-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="9816a-155">`[ResourceType <String>]`: A szülőerőforrás erőforrástípusa</span><span class="sxs-lookup"><span data-stu-id="9816a-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="9816a-156">`[SolutionName <String>]`: Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="9816a-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="9816a-157">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9816a-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9816a-158">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9816a-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9816a-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9816a-159">RELATED LINKS</span></span>

