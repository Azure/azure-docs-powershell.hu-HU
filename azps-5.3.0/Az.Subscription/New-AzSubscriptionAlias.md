---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384214"
---
# <span data-ttu-id="01dd4-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="01dd4-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="01dd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="01dd4-103">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="01dd4-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="01dd4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01dd4-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01dd4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01dd4-105">DESCRIPTION</span></span>
<span data-ttu-id="01dd4-106">A **New-AzSubscriptionAlias** parancsmag új aliast és előfizetést hoz létre</span><span class="sxs-lookup"><span data-stu-id="01dd4-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="01dd4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01dd4-107">EXAMPLES</span></span>

### <span data-ttu-id="01dd4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="01dd4-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="01dd4-109">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="01dd4-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="01dd4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01dd4-110">PARAMETERS</span></span>

### <span data-ttu-id="01dd4-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="01dd4-111">-AliasName</span></span>
<span data-ttu-id="01dd4-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="01dd4-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="01dd4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01dd4-113">-AsJob</span></span>
<span data-ttu-id="01dd4-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="01dd4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01dd4-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="01dd4-115">-BillingScope</span></span>
<span data-ttu-id="01dd4-116">Számlázási hatókör</span><span class="sxs-lookup"><span data-stu-id="01dd4-116">Billing Scope</span></span>

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

### <span data-ttu-id="01dd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dd4-117">-DefaultProfile</span></span>
<span data-ttu-id="01dd4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01dd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dd4-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="01dd4-119">-ResellerId</span></span>
<span data-ttu-id="01dd4-120">Viszonteladói azonosító</span><span class="sxs-lookup"><span data-stu-id="01dd4-120">Reseller Id</span></span>

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

### <span data-ttu-id="01dd4-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01dd4-121">-SubscriptionId</span></span>
<span data-ttu-id="01dd4-122">Meglévő előfizetésazonosító</span><span class="sxs-lookup"><span data-stu-id="01dd4-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="01dd4-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="01dd4-123">-SubscriptionName</span></span>
<span data-ttu-id="01dd4-124">Az előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="01dd4-124">Name of the subscription</span></span>

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

### <span data-ttu-id="01dd4-125">-Workload</span><span class="sxs-lookup"><span data-stu-id="01dd4-125">-Workload</span></span>
<span data-ttu-id="01dd4-126">Munkaterhelés típusa</span><span class="sxs-lookup"><span data-stu-id="01dd4-126">Type of Workload</span></span>

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

### <span data-ttu-id="01dd4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01dd4-127">-Confirm</span></span>
<span data-ttu-id="01dd4-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01dd4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01dd4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01dd4-129">-WhatIf</span></span>
<span data-ttu-id="01dd4-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01dd4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01dd4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01dd4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01dd4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dd4-132">CommonParameters</span></span>
<span data-ttu-id="01dd4-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01dd4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dd4-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01dd4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dd4-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01dd4-135">INPUTS</span></span>

### <span data-ttu-id="01dd4-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="01dd4-136">None</span></span>

## <span data-ttu-id="01dd4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01dd4-137">OUTPUTS</span></span>

### <span data-ttu-id="01dd4-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="01dd4-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="01dd4-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01dd4-139">NOTES</span></span>

## <span data-ttu-id="01dd4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01dd4-140">RELATED LINKS</span></span>
