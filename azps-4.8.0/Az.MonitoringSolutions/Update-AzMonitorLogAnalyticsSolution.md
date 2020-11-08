---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183479"
---
# <span data-ttu-id="8d424-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="8d424-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="8d424-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d424-102">SYNOPSIS</span></span>
<span data-ttu-id="8d424-103">Frissítheti egy megoldás címkéit.</span><span class="sxs-lookup"><span data-stu-id="8d424-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="8d424-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d424-104">SYNTAX</span></span>

### <span data-ttu-id="8d424-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d424-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d424-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8d424-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d424-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d424-107">DESCRIPTION</span></span>
<span data-ttu-id="8d424-108">Frissítheti egy megoldás címkéit.</span><span class="sxs-lookup"><span data-stu-id="8d424-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="8d424-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8d424-109">EXAMPLES</span></span>

### <span data-ttu-id="8d424-110">1. példa: a monitor naplózási elemzési megoldásának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="8d424-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="8d424-111">Ez a parancs név szerint frissíti a monitor log-elemzési megoldását.</span><span class="sxs-lookup"><span data-stu-id="8d424-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="8d424-112">2. példa: a monitor log-elemzési megoldásának frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="8d424-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="8d424-113">Ez a parancs objektum alapján frissíti a monitor log-elemzési megoldását.</span><span class="sxs-lookup"><span data-stu-id="8d424-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="8d424-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d424-114">PARAMETERS</span></span>

### <span data-ttu-id="8d424-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d424-115">-DefaultProfile</span></span>
<span data-ttu-id="8d424-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d424-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d424-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d424-117">-InputObject</span></span>
<span data-ttu-id="8d424-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d424-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8d424-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d424-119">-Name</span></span>
<span data-ttu-id="8d424-120">Felhasználói megoldás neve</span><span class="sxs-lookup"><span data-stu-id="8d424-120">User Solution Name.</span></span>

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

### <span data-ttu-id="8d424-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d424-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d424-122">A beolvasott erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d424-122">The name of the resource group to get.</span></span>
<span data-ttu-id="8d424-123">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="8d424-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d424-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d424-124">-SubscriptionId</span></span>
<span data-ttu-id="8d424-125">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8d424-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d424-126">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8d424-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8d424-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="8d424-127">-Tag</span></span>
<span data-ttu-id="8d424-128">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="8d424-128">Resource tags</span></span>

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

### <span data-ttu-id="8d424-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d424-129">-Confirm</span></span>
<span data-ttu-id="8d424-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d424-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d424-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d424-131">-WhatIf</span></span>
<span data-ttu-id="8d424-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d424-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d424-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d424-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d424-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d424-134">CommonParameters</span></span>
<span data-ttu-id="8d424-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d424-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d424-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d424-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d424-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d424-137">INPUTS</span></span>

### <span data-ttu-id="8d424-138">Microsoft. Azure. PowerShell. parancsmagok. MonitoringSolutions. models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="8d424-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="8d424-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d424-139">OUTPUTS</span></span>

### <span data-ttu-id="8d424-140">Microsoft. Azure. PowerShell. parancsmagok. MonitoringSolutions. modellek. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="8d424-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="8d424-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d424-141">NOTES</span></span>

<span data-ttu-id="8d424-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8d424-142">ALIASES</span></span>

<span data-ttu-id="8d424-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="8d424-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d424-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8d424-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d424-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8d424-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d424-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="8d424-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d424-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8d424-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d424-148">`[ManagementAssociationName <String>]`: A felhasználó ManagementAssociation neve.</span><span class="sxs-lookup"><span data-stu-id="8d424-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="8d424-149">`[ManagementConfigurationName <String>]`: Felhasználókezelő konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="8d424-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="8d424-150">`[ProviderName <String>]`: Szolgáltató neve a szülő erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="8d424-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="8d424-151">`[ResourceGroupName <String>]`: A beolvasott erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d424-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="8d424-152">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="8d424-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d424-153">`[ResourceName <String>]`: Szülő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8d424-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="8d424-154">`[ResourceType <String>]`: Erőforrás típusa a szülő erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="8d424-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="8d424-155">`[SolutionName <String>]`: Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="8d424-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="8d424-156">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8d424-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8d424-157">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8d424-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8d424-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d424-158">RELATED LINKS</span></span>

