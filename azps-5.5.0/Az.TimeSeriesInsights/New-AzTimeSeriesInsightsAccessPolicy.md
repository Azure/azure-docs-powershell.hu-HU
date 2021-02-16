---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164522"
---
# <span data-ttu-id="00f7b-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="00f7b-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="00f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="00f7b-103">Hozzáférési házirend létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="00f7b-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="00f7b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00f7b-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00f7b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="00f7b-106">Hozzáférési házirend létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="00f7b-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="00f7b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="00f7b-108">1. példa: Hozzáférési házirend létrehozása egy adott környezethez</span><span class="sxs-lookup"><span data-stu-id="00f7b-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="00f7b-109">Ez a parancs hozzáférési házirendet hoz létre egy adott környezethez.</span><span class="sxs-lookup"><span data-stu-id="00f7b-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="00f7b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00f7b-110">PARAMETERS</span></span>

### <span data-ttu-id="00f7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f7b-111">-DefaultProfile</span></span>
<span data-ttu-id="00f7b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00f7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f7b-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="00f7b-113">-Description</span></span>
<span data-ttu-id="00f7b-114">A hozzáférési házirend leírása.</span><span class="sxs-lookup"><span data-stu-id="00f7b-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="00f7b-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="00f7b-115">-EnvironmentName</span></span>
<span data-ttu-id="00f7b-116">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="00f7b-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="00f7b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="00f7b-117">-Name</span></span>
<span data-ttu-id="00f7b-118">A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="00f7b-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="00f7b-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="00f7b-119">-PrincipalObjectId</span></span>
<span data-ttu-id="00f7b-120">The objectId of the principal in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00f7b-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="00f7b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f7b-121">-ResourceGroupName</span></span>
<span data-ttu-id="00f7b-122">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="00f7b-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="00f7b-123">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="00f7b-123">-Role</span></span>
<span data-ttu-id="00f7b-124">A környezetben hozzárendelt szerepkörök listája.</span><span class="sxs-lookup"><span data-stu-id="00f7b-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="00f7b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00f7b-125">-SubscriptionId</span></span>
<span data-ttu-id="00f7b-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00f7b-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="00f7b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00f7b-127">-Confirm</span></span>
<span data-ttu-id="00f7b-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="00f7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00f7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f7b-129">-WhatIf</span></span>
<span data-ttu-id="00f7b-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="00f7b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00f7b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00f7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00f7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f7b-132">CommonParameters</span></span>
<span data-ttu-id="00f7b-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f7b-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00f7b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f7b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00f7b-135">INPUTS</span></span>

## <span data-ttu-id="00f7b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00f7b-136">OUTPUTS</span></span>

### <span data-ttu-id="00f7b-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="00f7b-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="00f7b-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00f7b-138">NOTES</span></span>

<span data-ttu-id="00f7b-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="00f7b-139">ALIASES</span></span>

## <span data-ttu-id="00f7b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00f7b-140">RELATED LINKS</span></span>

