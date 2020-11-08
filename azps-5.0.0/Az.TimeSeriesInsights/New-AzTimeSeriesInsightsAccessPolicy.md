---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194990"
---
# <span data-ttu-id="83f79-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="83f79-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="83f79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83f79-102">SYNOPSIS</span></span>
<span data-ttu-id="83f79-103">Hozzáférési házirend létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="83f79-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="83f79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83f79-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83f79-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83f79-105">DESCRIPTION</span></span>
<span data-ttu-id="83f79-106">Hozzáférési házirend létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="83f79-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="83f79-107">Példák</span><span class="sxs-lookup"><span data-stu-id="83f79-107">EXAMPLES</span></span>

### <span data-ttu-id="83f79-108">Példa 1: hozzáférési házirend létrehozása meghatározott környezethez</span><span class="sxs-lookup"><span data-stu-id="83f79-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="83f79-109">Ez a parancs egy meghatározott környezethez hoz létre hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="83f79-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="83f79-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83f79-110">PARAMETERS</span></span>

### <span data-ttu-id="83f79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f79-111">-DefaultProfile</span></span>
<span data-ttu-id="83f79-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83f79-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f79-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="83f79-113">-Description</span></span>
<span data-ttu-id="83f79-114">A hozzáférési házirend leírása.</span><span class="sxs-lookup"><span data-stu-id="83f79-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="83f79-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="83f79-115">-EnvironmentName</span></span>
<span data-ttu-id="83f79-116">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="83f79-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83f79-117">-Name</span></span>
<span data-ttu-id="83f79-118">A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="83f79-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="83f79-119">-PrincipalObjectId</span></span>
<span data-ttu-id="83f79-120">A objectId az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="83f79-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="83f79-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f79-121">-ResourceGroupName</span></span>
<span data-ttu-id="83f79-122">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="83f79-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="83f79-123">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="83f79-123">-Role</span></span>
<span data-ttu-id="83f79-124">Azon szerepkörök listája, amelyeket a megbízó a környezetre kiosztott.</span><span class="sxs-lookup"><span data-stu-id="83f79-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="83f79-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83f79-125">-SubscriptionId</span></span>
<span data-ttu-id="83f79-126">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="83f79-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="83f79-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83f79-127">-Confirm</span></span>
<span data-ttu-id="83f79-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83f79-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f79-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f79-129">-WhatIf</span></span>
<span data-ttu-id="83f79-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83f79-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f79-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83f79-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f79-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f79-132">CommonParameters</span></span>
<span data-ttu-id="83f79-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83f79-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f79-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83f79-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f79-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83f79-135">INPUTS</span></span>

## <span data-ttu-id="83f79-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83f79-136">OUTPUTS</span></span>

### <span data-ttu-id="83f79-137">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="83f79-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="83f79-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83f79-138">NOTES</span></span>

<span data-ttu-id="83f79-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="83f79-139">ALIASES</span></span>

## <span data-ttu-id="83f79-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83f79-140">RELATED LINKS</span></span>

