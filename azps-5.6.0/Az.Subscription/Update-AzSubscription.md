---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 0fe030e3ef4dfcb8e43ba436d37d582871e55a5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930682"
---
# <span data-ttu-id="e6cb3-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="e6cb3-101">Update-AzSubscription</span></span>

## <span data-ttu-id="e6cb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cb3-103">Azure-előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="e6cb3-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="e6cb3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6cb3-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6cb3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cb3-106">Az **Update-AzSubscription** parancsmag frissíti az Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="e6cb3-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="e6cb3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6cb3-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cb3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6cb3-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="e6cb3-109">Az előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="e6cb3-109">Updates the subscription</span></span>

## <span data-ttu-id="e6cb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6cb3-110">PARAMETERS</span></span>

### <span data-ttu-id="e6cb3-111">-Művelet</span><span class="sxs-lookup"><span data-stu-id="e6cb3-111">-Action</span></span>
<span data-ttu-id="e6cb3-112">Az előfizetésen végre kell hajtanunk egy műveletet</span><span class="sxs-lookup"><span data-stu-id="e6cb3-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="e6cb3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6cb3-113">-AsJob</span></span>
<span data-ttu-id="e6cb3-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6cb3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6cb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cb3-115">-DefaultProfile</span></span>
<span data-ttu-id="e6cb3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6cb3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e6cb3-117">-Name</span></span>
<span data-ttu-id="e6cb3-118">Az előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="e6cb3-118">Name of the subscription</span></span>

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

### <span data-ttu-id="e6cb3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6cb3-119">-SubscriptionId</span></span>
<span data-ttu-id="e6cb3-120">Frissítend kell az előfizetésazonosítót</span><span class="sxs-lookup"><span data-stu-id="e6cb3-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="e6cb3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6cb3-121">-Confirm</span></span>
<span data-ttu-id="e6cb3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6cb3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cb3-123">-WhatIf</span></span>
<span data-ttu-id="e6cb3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6cb3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6cb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cb3-126">CommonParameters</span></span>
<span data-ttu-id="e6cb3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cb3-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6cb3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cb3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6cb3-129">INPUTS</span></span>

### <span data-ttu-id="e6cb3-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="e6cb3-130">None</span></span>

## <span data-ttu-id="e6cb3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6cb3-131">OUTPUTS</span></span>

### <span data-ttu-id="e6cb3-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="e6cb3-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="e6cb3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6cb3-133">NOTES</span></span>

## <span data-ttu-id="e6cb3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6cb3-134">RELATED LINKS</span></span>
