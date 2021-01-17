---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360876"
---
# <span data-ttu-id="38f0e-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38f0e-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="38f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="38f0e-103">Beveszi a megadott nevű hozzáférési házirendet a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="38f0e-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="38f0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38f0e-104">SYNTAX</span></span>

### <span data-ttu-id="38f0e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38f0e-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="38f0e-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="38f0e-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="38f0e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38f0e-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="38f0e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38f0e-108">DESCRIPTION</span></span>
<span data-ttu-id="38f0e-109">Beveszi a megadott nevű hozzáférési házirendet a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="38f0e-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="38f0e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38f0e-110">EXAMPLES</span></span>

### <span data-ttu-id="38f0e-111">1. példa: Az összes hozzáférési házirend felsorolása egy adott környezetben</span><span class="sxs-lookup"><span data-stu-id="38f0e-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="38f0e-112">Ez a parancs felsorolja az adott környezetben található összes hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="38f0e-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="38f0e-113">2. példa: Megadott hozzáférési házirend lekért neve</span><span class="sxs-lookup"><span data-stu-id="38f0e-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="38f0e-114">Ez a parancs egy megadott hozzáférési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="38f0e-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="38f0e-115">3. példa: Megadott hozzáférési házirend lekérte objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="38f0e-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="38f0e-116">Ez a parancs egy megadott hozzáférési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="38f0e-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="38f0e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38f0e-117">PARAMETERS</span></span>

### <span data-ttu-id="38f0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f0e-118">-DefaultProfile</span></span>
<span data-ttu-id="38f0e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38f0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38f0e-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="38f0e-120">-EnvironmentName</span></span>
<span data-ttu-id="38f0e-121">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="38f0e-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="38f0e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38f0e-122">-InputObject</span></span>
<span data-ttu-id="38f0e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="38f0e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38f0e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="38f0e-124">-Name</span></span>
<span data-ttu-id="38f0e-125">A megadott környezethez társított Time Series Insights hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="38f0e-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f0e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f0e-126">-ResourceGroupName</span></span>
<span data-ttu-id="38f0e-127">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="38f0e-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="38f0e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38f0e-128">-SubscriptionId</span></span>
<span data-ttu-id="38f0e-129">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38f0e-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f0e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f0e-130">CommonParameters</span></span>
<span data-ttu-id="38f0e-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f0e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f0e-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38f0e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f0e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38f0e-133">INPUTS</span></span>

### <span data-ttu-id="38f0e-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="38f0e-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="38f0e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38f0e-135">OUTPUTS</span></span>

### <span data-ttu-id="38f0e-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="38f0e-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="38f0e-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38f0e-137">NOTES</span></span>

<span data-ttu-id="38f0e-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="38f0e-138">ALIASES</span></span>

<span data-ttu-id="38f0e-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="38f0e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38f0e-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="38f0e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38f0e-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38f0e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38f0e-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="38f0e-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38f0e-143">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="38f0e-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="38f0e-144">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="38f0e-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="38f0e-145">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="38f0e-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="38f0e-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="38f0e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38f0e-147">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="38f0e-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="38f0e-148">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="38f0e-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="38f0e-149">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38f0e-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="38f0e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38f0e-150">RELATED LINKS</span></span>

