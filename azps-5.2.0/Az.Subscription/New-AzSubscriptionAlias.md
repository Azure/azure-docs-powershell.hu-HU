---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367946"
---
# <span data-ttu-id="cd1f3-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="cd1f3-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="cd1f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1f3-103">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="cd1f3-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="cd1f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd1f3-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd1f3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="cd1f3-106">A **New-AzSubscriptionAlias** parancsmag új aliast és előfizetést hoz létre</span><span class="sxs-lookup"><span data-stu-id="cd1f3-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="cd1f3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd1f3-107">EXAMPLES</span></span>

### <span data-ttu-id="cd1f3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cd1f3-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="cd1f3-109">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="cd1f3-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="cd1f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd1f3-110">PARAMETERS</span></span>

### <span data-ttu-id="cd1f3-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="cd1f3-111">-AliasName</span></span>
<span data-ttu-id="cd1f3-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="cd1f3-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="cd1f3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd1f3-113">-AsJob</span></span>
<span data-ttu-id="cd1f3-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cd1f3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd1f3-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="cd1f3-115">-BillingScope</span></span>
<span data-ttu-id="cd1f3-116">Számlázási hatókör</span><span class="sxs-lookup"><span data-stu-id="cd1f3-116">Billing Scope</span></span>

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

### <span data-ttu-id="cd1f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1f3-117">-DefaultProfile</span></span>
<span data-ttu-id="cd1f3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd1f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd1f3-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="cd1f3-119">-ResellerId</span></span>
<span data-ttu-id="cd1f3-120">Viszonteladói azonosító</span><span class="sxs-lookup"><span data-stu-id="cd1f3-120">Reseller Id</span></span>

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

### <span data-ttu-id="cd1f3-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd1f3-121">-SubscriptionId</span></span>
<span data-ttu-id="cd1f3-122">Meglévő előfizetésazonosító</span><span class="sxs-lookup"><span data-stu-id="cd1f3-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="cd1f3-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cd1f3-123">-SubscriptionName</span></span>
<span data-ttu-id="cd1f3-124">Az előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="cd1f3-124">Name of the subscription</span></span>

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

### <span data-ttu-id="cd1f3-125">-Workload</span><span class="sxs-lookup"><span data-stu-id="cd1f3-125">-Workload</span></span>
<span data-ttu-id="cd1f3-126">Munkaterhelés típusa</span><span class="sxs-lookup"><span data-stu-id="cd1f3-126">Type of Workload</span></span>

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

### <span data-ttu-id="cd1f3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd1f3-127">-Confirm</span></span>
<span data-ttu-id="cd1f3-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd1f3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd1f3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1f3-129">-WhatIf</span></span>
<span data-ttu-id="cd1f3-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd1f3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd1f3-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd1f3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd1f3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1f3-132">CommonParameters</span></span>
<span data-ttu-id="cd1f3-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1f3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1f3-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd1f3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1f3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd1f3-135">INPUTS</span></span>

### <span data-ttu-id="cd1f3-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="cd1f3-136">None</span></span>

## <span data-ttu-id="cd1f3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd1f3-137">OUTPUTS</span></span>

### <span data-ttu-id="cd1f3-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cd1f3-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="cd1f3-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd1f3-139">NOTES</span></span>

## <span data-ttu-id="cd1f3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd1f3-140">RELATED LINKS</span></span>
