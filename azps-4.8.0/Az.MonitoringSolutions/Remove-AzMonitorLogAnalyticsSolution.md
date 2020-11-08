---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024689"
---
# <span data-ttu-id="3456e-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="3456e-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="3456e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3456e-102">SYNOPSIS</span></span>
<span data-ttu-id="3456e-103">Törli a megoldást az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3456e-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="3456e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3456e-104">SYNTAX</span></span>

### <span data-ttu-id="3456e-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3456e-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3456e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3456e-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3456e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3456e-107">DESCRIPTION</span></span>
<span data-ttu-id="3456e-108">Törli a megoldást az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3456e-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="3456e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3456e-109">EXAMPLES</span></span>

### <span data-ttu-id="3456e-110">1. példa: a monitor log Analytics-megoldás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="3456e-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="3456e-111">Ez a parancs a monitor log Analytics-megoldást név szerint távolítja el.</span><span class="sxs-lookup"><span data-stu-id="3456e-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="3456e-112">2. példa: a monitor log-elemzési megoldás eltávolítása objektumból</span><span class="sxs-lookup"><span data-stu-id="3456e-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="3456e-113">Ez a parancs objektum alapján távolítja el a monitor log-elemzési megoldását.</span><span class="sxs-lookup"><span data-stu-id="3456e-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="3456e-114">3. példa: a monitor log-elemzési megoldás eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3456e-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="3456e-115">Ez a parancs a monitor log-elemzési megoldását pipeline segítségével távolítja el.</span><span class="sxs-lookup"><span data-stu-id="3456e-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="3456e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3456e-116">PARAMETERS</span></span>

### <span data-ttu-id="3456e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3456e-117">-DefaultProfile</span></span>
<span data-ttu-id="3456e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3456e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3456e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3456e-119">-InputObject</span></span>
<span data-ttu-id="3456e-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3456e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3456e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3456e-121">-Name</span></span>
<span data-ttu-id="3456e-122">Felhasználói megoldás neve</span><span class="sxs-lookup"><span data-stu-id="3456e-122">User Solution Name.</span></span>

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

### <span data-ttu-id="3456e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3456e-123">-PassThru</span></span>
<span data-ttu-id="3456e-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="3456e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3456e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3456e-125">-ResourceGroupName</span></span>
<span data-ttu-id="3456e-126">A beolvasott erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3456e-126">The name of the resource group to get.</span></span>
<span data-ttu-id="3456e-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="3456e-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3456e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3456e-128">-SubscriptionId</span></span>
<span data-ttu-id="3456e-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3456e-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3456e-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3456e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3456e-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3456e-131">-Confirm</span></span>
<span data-ttu-id="3456e-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3456e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3456e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3456e-133">-WhatIf</span></span>
<span data-ttu-id="3456e-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3456e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3456e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3456e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3456e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3456e-136">CommonParameters</span></span>
<span data-ttu-id="3456e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3456e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3456e-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3456e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3456e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3456e-139">INPUTS</span></span>

### <span data-ttu-id="3456e-140">Microsoft. Azure. PowerShell. parancsmagok. MonitoringSolutions. models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="3456e-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="3456e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3456e-141">OUTPUTS</span></span>

### <span data-ttu-id="3456e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3456e-142">System.Boolean</span></span>

## <span data-ttu-id="3456e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3456e-143">NOTES</span></span>

<span data-ttu-id="3456e-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3456e-144">ALIASES</span></span>

<span data-ttu-id="3456e-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3456e-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3456e-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3456e-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3456e-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3456e-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3456e-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3456e-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3456e-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3456e-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3456e-150">`[ManagementAssociationName <String>]`: A felhasználó ManagementAssociation neve.</span><span class="sxs-lookup"><span data-stu-id="3456e-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="3456e-151">`[ManagementConfigurationName <String>]`: Felhasználókezelő konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="3456e-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="3456e-152">`[ProviderName <String>]`: Szolgáltató neve a szülő erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="3456e-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="3456e-153">`[ResourceGroupName <String>]`: A beolvasott erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3456e-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="3456e-154">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="3456e-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="3456e-155">`[ResourceName <String>]`: Szülő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3456e-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="3456e-156">`[ResourceType <String>]`: Erőforrás típusa a szülő erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="3456e-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="3456e-157">`[SolutionName <String>]`: Felhasználói megoldás neve.</span><span class="sxs-lookup"><span data-stu-id="3456e-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="3456e-158">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3456e-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3456e-159">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3456e-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3456e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3456e-160">RELATED LINKS</span></span>

