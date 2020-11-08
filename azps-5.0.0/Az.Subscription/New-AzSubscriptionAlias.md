---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195007"
---
# <span data-ttu-id="71eef-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="71eef-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="71eef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71eef-102">SYNOPSIS</span></span>
<span data-ttu-id="71eef-103">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="71eef-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="71eef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71eef-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71eef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71eef-105">DESCRIPTION</span></span>
<span data-ttu-id="71eef-106">A **New-AzSubscriptionAlias** parancsmag új aliast és előfizetést hoz létre</span><span class="sxs-lookup"><span data-stu-id="71eef-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="71eef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71eef-107">EXAMPLES</span></span>

### <span data-ttu-id="71eef-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71eef-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="71eef-109">Új alias és előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="71eef-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="71eef-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71eef-110">PARAMETERS</span></span>

### <span data-ttu-id="71eef-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="71eef-111">-AliasName</span></span>
<span data-ttu-id="71eef-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="71eef-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="71eef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71eef-113">-AsJob</span></span>
<span data-ttu-id="71eef-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71eef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71eef-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="71eef-115">-BillingScope</span></span>
<span data-ttu-id="71eef-116">Számlázási tartomány</span><span class="sxs-lookup"><span data-stu-id="71eef-116">Billing Scope</span></span>

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

### <span data-ttu-id="71eef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71eef-117">-DefaultProfile</span></span>
<span data-ttu-id="71eef-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71eef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71eef-119">-Viszonteladó azonosítója</span><span class="sxs-lookup"><span data-stu-id="71eef-119">-ResellerId</span></span>
<span data-ttu-id="71eef-120">Viszonteladói azonosító</span><span class="sxs-lookup"><span data-stu-id="71eef-120">Reseller Id</span></span>

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

### <span data-ttu-id="71eef-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71eef-121">-SubscriptionId</span></span>
<span data-ttu-id="71eef-122">Meglévő előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="71eef-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="71eef-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="71eef-123">-SubscriptionName</span></span>
<span data-ttu-id="71eef-124">Az előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="71eef-124">Name of the subscription</span></span>

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

### <span data-ttu-id="71eef-125">-Munkaterhelés</span><span class="sxs-lookup"><span data-stu-id="71eef-125">-Workload</span></span>
<span data-ttu-id="71eef-126">A munkaterhelés típusa</span><span class="sxs-lookup"><span data-stu-id="71eef-126">Type of Workload</span></span>

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

### <span data-ttu-id="71eef-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71eef-127">-Confirm</span></span>
<span data-ttu-id="71eef-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71eef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71eef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71eef-129">-WhatIf</span></span>
<span data-ttu-id="71eef-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71eef-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71eef-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71eef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71eef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71eef-132">CommonParameters</span></span>
<span data-ttu-id="71eef-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71eef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71eef-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="71eef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71eef-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71eef-135">INPUTS</span></span>

### <span data-ttu-id="71eef-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="71eef-136">None</span></span>

## <span data-ttu-id="71eef-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71eef-137">OUTPUTS</span></span>

### <span data-ttu-id="71eef-138">Microsoft. Azure. Command. előfizetés. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="71eef-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="71eef-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71eef-139">NOTES</span></span>

## <span data-ttu-id="71eef-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71eef-140">RELATED LINKS</span></span>
