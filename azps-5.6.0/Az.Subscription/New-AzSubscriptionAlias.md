---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 30c90d4b04c6c32144946cbdf98c59991133dbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015829"
---
# <span data-ttu-id="63c51-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="63c51-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="63c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63c51-102">SYNOPSIS</span></span>
<span data-ttu-id="63c51-103">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="63c51-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="63c51-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63c51-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63c51-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63c51-105">DESCRIPTION</span></span>
<span data-ttu-id="63c51-106">A **New-AzSubscriptionAlias** parancsmag új aliast és előfizetést hoz létre</span><span class="sxs-lookup"><span data-stu-id="63c51-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="63c51-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63c51-107">EXAMPLES</span></span>

### <span data-ttu-id="63c51-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="63c51-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="63c51-109">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="63c51-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="63c51-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63c51-110">PARAMETERS</span></span>

### <span data-ttu-id="63c51-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="63c51-111">-AliasName</span></span>
<span data-ttu-id="63c51-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="63c51-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="63c51-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63c51-113">-AsJob</span></span>
<span data-ttu-id="63c51-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="63c51-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63c51-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="63c51-115">-BillingScope</span></span>
<span data-ttu-id="63c51-116">Számlázási hatókör</span><span class="sxs-lookup"><span data-stu-id="63c51-116">Billing Scope</span></span>

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

### <span data-ttu-id="63c51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c51-117">-DefaultProfile</span></span>
<span data-ttu-id="63c51-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63c51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63c51-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="63c51-119">-ResellerId</span></span>
<span data-ttu-id="63c51-120">Viszonteladói azonosító</span><span class="sxs-lookup"><span data-stu-id="63c51-120">Reseller Id</span></span>

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

### <span data-ttu-id="63c51-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63c51-121">-SubscriptionId</span></span>
<span data-ttu-id="63c51-122">Meglévő előfizetésazonosító</span><span class="sxs-lookup"><span data-stu-id="63c51-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="63c51-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="63c51-123">-SubscriptionName</span></span>
<span data-ttu-id="63c51-124">Az előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="63c51-124">Name of the subscription</span></span>

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

### <span data-ttu-id="63c51-125">-Workload</span><span class="sxs-lookup"><span data-stu-id="63c51-125">-Workload</span></span>
<span data-ttu-id="63c51-126">Munkaterhelés típusa</span><span class="sxs-lookup"><span data-stu-id="63c51-126">Type of Workload</span></span>

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

### <span data-ttu-id="63c51-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63c51-127">-Confirm</span></span>
<span data-ttu-id="63c51-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="63c51-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63c51-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63c51-129">-WhatIf</span></span>
<span data-ttu-id="63c51-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="63c51-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63c51-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63c51-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63c51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c51-132">CommonParameters</span></span>
<span data-ttu-id="63c51-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c51-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63c51-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c51-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63c51-135">INPUTS</span></span>

### <span data-ttu-id="63c51-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="63c51-136">None</span></span>

## <span data-ttu-id="63c51-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63c51-137">OUTPUTS</span></span>

### <span data-ttu-id="63c51-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="63c51-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="63c51-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63c51-139">NOTES</span></span>

## <span data-ttu-id="63c51-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63c51-140">RELATED LINKS</span></span>
