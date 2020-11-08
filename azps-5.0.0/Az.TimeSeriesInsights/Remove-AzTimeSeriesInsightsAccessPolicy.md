---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186496"
---
# <span data-ttu-id="f2893-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2893-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="f2893-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2893-102">SYNOPSIS</span></span>
<span data-ttu-id="f2893-103">A megadott névvel rendelkező hozzáférési házirend törlése a megadott előfizetéshez, erőforrás csoporthoz és környezethez</span><span class="sxs-lookup"><span data-stu-id="f2893-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="f2893-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2893-104">SYNTAX</span></span>

### <span data-ttu-id="f2893-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2893-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2893-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2893-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2893-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2893-107">DESCRIPTION</span></span>
<span data-ttu-id="f2893-108">A megadott névvel rendelkező hozzáférési házirend törlése a megadott előfizetéshez, erőforrás csoporthoz és környezethez</span><span class="sxs-lookup"><span data-stu-id="f2893-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="f2893-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2893-109">EXAMPLES</span></span>

### <span data-ttu-id="f2893-110">Példa 1: meghatározott hozzáférési házirend eltávolítása névvel</span><span class="sxs-lookup"><span data-stu-id="f2893-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="f2893-111">Ez a parancs eltávolítja a megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="f2893-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="f2893-112">2. példa: meghatározott hozzáférési házirend eltávolítása objektumból</span><span class="sxs-lookup"><span data-stu-id="f2893-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="f2893-113">Ez a parancs eltávolítja a megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="f2893-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="f2893-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2893-114">PARAMETERS</span></span>

### <span data-ttu-id="f2893-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2893-115">-DefaultProfile</span></span>
<span data-ttu-id="f2893-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2893-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2893-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="f2893-117">-EnvironmentName</span></span>
<span data-ttu-id="f2893-118">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="f2893-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f2893-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2893-119">-InputObject</span></span>
<span data-ttu-id="f2893-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2893-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2893-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2893-121">-Name</span></span>
<span data-ttu-id="f2893-122">A megadott környezethez társított idősorok elérési házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="f2893-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2893-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2893-123">-PassThru</span></span>
<span data-ttu-id="f2893-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f2893-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2893-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2893-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2893-126">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f2893-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f2893-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2893-127">-SubscriptionId</span></span>
<span data-ttu-id="f2893-128">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="f2893-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f2893-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f2893-129">-Confirm</span></span>
<span data-ttu-id="f2893-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f2893-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2893-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2893-131">-WhatIf</span></span>
<span data-ttu-id="f2893-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f2893-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2893-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2893-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2893-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2893-134">CommonParameters</span></span>
<span data-ttu-id="f2893-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2893-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2893-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2893-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2893-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2893-137">INPUTS</span></span>

### <span data-ttu-id="f2893-138">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="f2893-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f2893-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2893-139">OUTPUTS</span></span>

### <span data-ttu-id="f2893-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2893-140">System.Boolean</span></span>

## <span data-ttu-id="f2893-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2893-141">NOTES</span></span>

<span data-ttu-id="f2893-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f2893-142">ALIASES</span></span>

<span data-ttu-id="f2893-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f2893-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2893-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f2893-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2893-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f2893-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2893-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f2893-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2893-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="f2893-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f2893-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="f2893-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f2893-149">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="f2893-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f2893-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f2893-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2893-151">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="f2893-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f2893-152">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2893-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f2893-153">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f2893-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f2893-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2893-154">RELATED LINKS</span></span>

