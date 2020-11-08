---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025045"
---
# <span data-ttu-id="b15eb-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b15eb-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="b15eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b15eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b15eb-103">A megadott környezetben kapja meg a megadott nevű hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="b15eb-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b15eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b15eb-104">SYNTAX</span></span>

### <span data-ttu-id="b15eb-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b15eb-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b15eb-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b15eb-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b15eb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b15eb-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b15eb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b15eb-108">DESCRIPTION</span></span>
<span data-ttu-id="b15eb-109">A megadott környezetben kapja meg a megadott nevű hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="b15eb-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b15eb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b15eb-110">EXAMPLES</span></span>

### <span data-ttu-id="b15eb-111">Példa 1: az összes Access-házirend listázása a megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="b15eb-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b15eb-112">Ez a parancs felsorolja az összes Access-házirendet a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="b15eb-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="b15eb-113">2. példa: megadott hozzáférési házirend beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="b15eb-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b15eb-114">Ez a parancs a megadott hozzáférési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b15eb-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="b15eb-115">3. példa: meghatározott hozzáférési házirend beszerzése objektum alapján</span><span class="sxs-lookup"><span data-stu-id="b15eb-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b15eb-116">Ez a parancs a megadott hozzáférési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b15eb-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="b15eb-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b15eb-117">PARAMETERS</span></span>

### <span data-ttu-id="b15eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15eb-118">-DefaultProfile</span></span>
<span data-ttu-id="b15eb-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b15eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b15eb-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b15eb-120">-EnvironmentName</span></span>
<span data-ttu-id="b15eb-121">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="b15eb-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="b15eb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b15eb-122">-InputObject</span></span>
<span data-ttu-id="b15eb-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b15eb-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b15eb-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b15eb-124">-Name</span></span>
<span data-ttu-id="b15eb-125">A megadott környezethez társított idősorok elérési házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="b15eb-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="b15eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b15eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="b15eb-127">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b15eb-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="b15eb-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b15eb-128">-SubscriptionId</span></span>
<span data-ttu-id="b15eb-129">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="b15eb-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b15eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15eb-130">CommonParameters</span></span>
<span data-ttu-id="b15eb-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b15eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15eb-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b15eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15eb-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b15eb-133">INPUTS</span></span>

### <span data-ttu-id="b15eb-134">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="b15eb-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="b15eb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b15eb-135">OUTPUTS</span></span>

### <span data-ttu-id="b15eb-136">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="b15eb-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="b15eb-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b15eb-137">NOTES</span></span>

<span data-ttu-id="b15eb-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b15eb-138">ALIASES</span></span>

<span data-ttu-id="b15eb-139">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="b15eb-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b15eb-140">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b15eb-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b15eb-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b15eb-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b15eb-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b15eb-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b15eb-143">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="b15eb-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="b15eb-144">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="b15eb-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="b15eb-145">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="b15eb-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="b15eb-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b15eb-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b15eb-147">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="b15eb-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="b15eb-148">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b15eb-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="b15eb-149">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b15eb-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b15eb-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b15eb-150">RELATED LINKS</span></span>

