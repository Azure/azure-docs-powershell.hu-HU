---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195452"
---
# <span data-ttu-id="d4a02-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4a02-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="d4a02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4a02-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a02-103">A megadott névvel rendelkező környezet törlése a megadott előfizetés és erőforráscsoport szerint.</span><span class="sxs-lookup"><span data-stu-id="d4a02-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="d4a02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4a02-104">SYNTAX</span></span>

### <span data-ttu-id="d4a02-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4a02-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4a02-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4a02-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4a02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4a02-107">DESCRIPTION</span></span>
<span data-ttu-id="d4a02-108">A megadott névvel rendelkező környezet törlése a megadott előfizetés és erőforráscsoport szerint.</span><span class="sxs-lookup"><span data-stu-id="d4a02-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="d4a02-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d4a02-109">EXAMPLES</span></span>

### <span data-ttu-id="d4a02-110">1. példa: idősorozat-adatelemzési környezet eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="d4a02-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="d4a02-111">Ez a parancs eltávolítja az időbeli adatsorok környezetét.</span><span class="sxs-lookup"><span data-stu-id="d4a02-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="d4a02-112">2. példa: időbeli adatsorozatok objektum szerinti környezetének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4a02-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="d4a02-113">Ez a parancs eltávolítja az időbeli adatsorok környezetét.</span><span class="sxs-lookup"><span data-stu-id="d4a02-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="d4a02-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4a02-114">PARAMETERS</span></span>

### <span data-ttu-id="d4a02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a02-115">-DefaultProfile</span></span>
<span data-ttu-id="d4a02-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4a02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a02-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4a02-117">-InputObject</span></span>
<span data-ttu-id="d4a02-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4a02-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a02-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4a02-119">-Name</span></span>
<span data-ttu-id="d4a02-120">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="d4a02-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a02-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4a02-121">-PassThru</span></span>
<span data-ttu-id="d4a02-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="d4a02-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d4a02-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a02-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4a02-124">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d4a02-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="d4a02-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4a02-125">-SubscriptionId</span></span>
<span data-ttu-id="d4a02-126">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="d4a02-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d4a02-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4a02-127">-Confirm</span></span>
<span data-ttu-id="d4a02-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4a02-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a02-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a02-129">-WhatIf</span></span>
<span data-ttu-id="d4a02-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4a02-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a02-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4a02-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a02-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a02-132">CommonParameters</span></span>
<span data-ttu-id="d4a02-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4a02-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a02-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4a02-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a02-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4a02-135">INPUTS</span></span>

### <span data-ttu-id="d4a02-136">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="d4a02-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="d4a02-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4a02-137">OUTPUTS</span></span>

### <span data-ttu-id="d4a02-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4a02-138">System.Boolean</span></span>

## <span data-ttu-id="d4a02-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4a02-139">NOTES</span></span>

<span data-ttu-id="d4a02-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d4a02-140">ALIASES</span></span>

<span data-ttu-id="d4a02-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d4a02-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4a02-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d4a02-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4a02-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d4a02-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4a02-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d4a02-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4a02-145">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="d4a02-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="d4a02-146">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="d4a02-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="d4a02-147">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="d4a02-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="d4a02-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d4a02-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4a02-149">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="d4a02-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="d4a02-150">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4a02-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="d4a02-151">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d4a02-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d4a02-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4a02-152">RELATED LINKS</span></span>

