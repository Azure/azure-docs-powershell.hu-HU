---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183444"
---
# <span data-ttu-id="e62ab-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e62ab-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="e62ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e62ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e62ab-103">Hozzáférési házirend létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="e62ab-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="e62ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e62ab-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e62ab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e62ab-105">DESCRIPTION</span></span>
<span data-ttu-id="e62ab-106">Hozzáférési házirend létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="e62ab-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="e62ab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e62ab-107">EXAMPLES</span></span>

### <span data-ttu-id="e62ab-108">Példa 1: hozzáférési házirend létrehozása meghatározott környezethez</span><span class="sxs-lookup"><span data-stu-id="e62ab-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e62ab-109">Ez a parancs egy meghatározott környezethez hoz létre hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="e62ab-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="e62ab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e62ab-110">PARAMETERS</span></span>

### <span data-ttu-id="e62ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62ab-111">-DefaultProfile</span></span>
<span data-ttu-id="e62ab-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e62ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62ab-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e62ab-113">-Description</span></span>
<span data-ttu-id="e62ab-114">A hozzáférési házirend leírása.</span><span class="sxs-lookup"><span data-stu-id="e62ab-114">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ab-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e62ab-115">-EnvironmentName</span></span>
<span data-ttu-id="e62ab-116">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="e62ab-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ab-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e62ab-117">-Name</span></span>
<span data-ttu-id="e62ab-118">A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="e62ab-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ab-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="e62ab-119">-PrincipalObjectId</span></span>
<span data-ttu-id="e62ab-120">A objectId az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="e62ab-120">The objectId of the principal in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="e62ab-122">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e62ab-122">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ab-123">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="e62ab-123">-Role</span></span>
<span data-ttu-id="e62ab-124">Azon szerepkörök listája, amelyeket a megbízó a környezetre kiosztott.</span><span class="sxs-lookup"><span data-stu-id="e62ab-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ab-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e62ab-125">-SubscriptionId</span></span>
<span data-ttu-id="e62ab-126">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="e62ab-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ab-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e62ab-127">-Confirm</span></span>
<span data-ttu-id="e62ab-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e62ab-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62ab-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62ab-129">-WhatIf</span></span>
<span data-ttu-id="e62ab-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e62ab-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62ab-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e62ab-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62ab-132">CommonParameters</span></span>
<span data-ttu-id="e62ab-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e62ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62ab-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e62ab-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62ab-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e62ab-135">INPUTS</span></span>

## <span data-ttu-id="e62ab-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e62ab-136">OUTPUTS</span></span>

### <span data-ttu-id="e62ab-137">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="e62ab-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="e62ab-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e62ab-138">NOTES</span></span>

<span data-ttu-id="e62ab-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e62ab-139">ALIASES</span></span>

## <span data-ttu-id="e62ab-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e62ab-140">RELATED LINKS</span></span>

