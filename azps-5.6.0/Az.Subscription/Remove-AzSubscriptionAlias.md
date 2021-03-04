---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 2acca5ede1d6ef7e4a3767b87053fb356555993d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928441"
---
# <span data-ttu-id="216a0-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="216a0-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="216a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="216a0-102">SYNOPSIS</span></span>
<span data-ttu-id="216a0-103">Az előfizetés aliasának törlése</span><span class="sxs-lookup"><span data-stu-id="216a0-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="216a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="216a0-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="216a0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="216a0-105">DESCRIPTION</span></span>
<span data-ttu-id="216a0-106">A **Remove-AzSubscriptionAlias** parancsmag eltávolítja az előfizetés aliasát</span><span class="sxs-lookup"><span data-stu-id="216a0-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="216a0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="216a0-107">EXAMPLES</span></span>

### <span data-ttu-id="216a0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="216a0-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="216a0-109">Az előfizetés aliasának törlése</span><span class="sxs-lookup"><span data-stu-id="216a0-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="216a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="216a0-110">PARAMETERS</span></span>

### <span data-ttu-id="216a0-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="216a0-111">-AliasName</span></span>
<span data-ttu-id="216a0-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="216a0-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="216a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="216a0-113">-AsJob</span></span>
<span data-ttu-id="216a0-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="216a0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="216a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216a0-115">-DefaultProfile</span></span>
<span data-ttu-id="216a0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="216a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="216a0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="216a0-117">-Confirm</span></span>
<span data-ttu-id="216a0-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="216a0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="216a0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="216a0-119">-WhatIf</span></span>
<span data-ttu-id="216a0-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="216a0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="216a0-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="216a0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="216a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216a0-122">CommonParameters</span></span>
<span data-ttu-id="216a0-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="216a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216a0-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="216a0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216a0-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="216a0-125">INPUTS</span></span>

### <span data-ttu-id="216a0-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="216a0-126">None</span></span>

## <span data-ttu-id="216a0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="216a0-127">OUTPUTS</span></span>

### <span data-ttu-id="216a0-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="216a0-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="216a0-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="216a0-129">NOTES</span></span>

## <span data-ttu-id="216a0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="216a0-130">RELATED LINKS</span></span>
