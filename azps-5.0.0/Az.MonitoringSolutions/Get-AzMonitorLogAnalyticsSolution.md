---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195733"
---
# <span data-ttu-id="f0846-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="f0846-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="f0846-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0846-102">SYNOPSIS</span></span>
<span data-ttu-id="f0846-103">Lekéri a felhasználói megoldást.</span><span class="sxs-lookup"><span data-stu-id="f0846-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="f0846-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0846-104">SYNTAX</span></span>

### <span data-ttu-id="f0846-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0846-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0846-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f0846-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0846-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0846-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0846-108">Lista</span><span class="sxs-lookup"><span data-stu-id="f0846-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f0846-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0846-109">DESCRIPTION</span></span>
<span data-ttu-id="f0846-110">Lekéri a felhasználói megoldást.</span><span class="sxs-lookup"><span data-stu-id="f0846-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="f0846-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f0846-111">EXAMPLES</span></span>

### <span data-ttu-id="f0846-112">Példa 1: a monitor naplózási elemzési megoldásának beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="f0846-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f0846-113">Ez a parancs a monitor log Analytics-megoldását név szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="f0846-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="f0846-114">2. példa: a monitor naplózási elemzési megoldásának beszerzése erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="f0846-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="f0846-115">Ez a parancs erőforrás-azonosítóval kapja meg a monitor log-elemzési megoldását.</span><span class="sxs-lookup"><span data-stu-id="f0846-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="f0846-116">3. példa: a monitor naplózási elemzési megoldása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="f0846-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f0846-117">Ez a parancs objektumként a monitor log-elemzési megoldását kapja.</span><span class="sxs-lookup"><span data-stu-id="f0846-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="f0846-118">4. példa: a monitor minden naplózási Analytics-megoldásának beolvasása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="f0846-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f0846-119">Ez a parancs az erőforrás-csoportokban minden monitor log-elemzési megoldást kap.</span><span class="sxs-lookup"><span data-stu-id="f0846-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="f0846-120">Példa 5: a monitor minden naplózási Analytics-megoldásának beszerzése az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="f0846-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="f0846-121">Ez a parancs az előfizetések alatt naplózza az összes Analytics-megoldást.</span><span class="sxs-lookup"><span data-stu-id="f0846-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="f0846-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0846-122">PARAMETERS</span></span>

### <span data-ttu-id="f0846-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0846-123">-DefaultProfile</span></span>
<span data-ttu-id="f0846-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0846-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0846-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0846-125">-InputObject</span></span>
<span data-ttu-id="f0846-126">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f0846-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0846-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0846-127">-Name</span></span>
<span data-ttu-id="f0846-128">Felhasználói megoldás neve</span><span class="sxs-lookup"><span data-stu-id="f0846-128">User Solution Name.</span></span>

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

### <span data-ttu-id="f0846-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0846-129">-ResourceGroupName</span></span>
<span data-ttu-id="f0846-130">A beolvasott erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0846-130">The name of the resource group to get.</span></span>
<span data-ttu-id="f0846-131">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f0846-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f0846-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0846-132">-SubscriptionId</span></span>
<span data-ttu-id="f0846-133">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f0846-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f0846-134">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f0846-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f0846-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0846-135">CommonParameters</span></span>
<span data-ttu-id="f0846-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0846-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0846-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f0846-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0846-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0846-138">INPUTS</span></span>

### <span data-ttu-id="f0846-139">Microsoft. Azure. PowerShell. parancsmagok. MonitoringSolutions. models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="f0846-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="f0846-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0846-140">OUTPUTS</span></span>

### <span data-ttu-id="f0846-141">Microsoft. Azure. PowerShell. parancsmagok. MonitoringSolutions. modellek. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="f0846-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="f0846-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0846-142">NOTES</span></span>

<span data-ttu-id="f0846-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f0846-143">ALIASES</span></span>

<span data-ttu-id="f0846-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f0846-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0846-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f0846-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0846-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f0846-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0846-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f0846-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0846-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f0846-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0846-149">`[ManagementAssociationName <String>]`: A felhasználó ManagementAssociation neve.</span><span class="sxs-lookup"><span data-stu-id="f0846-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="f0846-150">`[ManagementConfigurationName <String>]`: Felhasználókezelő konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="f0846-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="f0846-151">`[ProviderName <String>]`: Szolgáltató neve a szülő erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="f0846-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="f0846-152">`[ResourceGroupName <String>]`: A beolvasott erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0846-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="f0846-153">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f0846-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="f0846-154">`[ResourceName <String>]`: Szülő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f0846-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="f0846-155">`[ResourceType <String>]`: Erőforrás típusa a szülő erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="f0846-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="f0846-156">`[SolutionName <String>]`: Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="f0846-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="f0846-157">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f0846-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f0846-158">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f0846-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f0846-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0846-159">RELATED LINKS</span></span>

