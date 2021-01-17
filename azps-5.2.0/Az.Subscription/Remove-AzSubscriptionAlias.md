---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367932"
---
# <span data-ttu-id="ada85-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="ada85-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="ada85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada85-102">SYNOPSIS</span></span>
<span data-ttu-id="ada85-103">Az előfizetés aliasának törlése</span><span class="sxs-lookup"><span data-stu-id="ada85-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="ada85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ada85-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ada85-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ada85-105">DESCRIPTION</span></span>
<span data-ttu-id="ada85-106">A **Remove-AzSubscriptionAlias** parancsmag eltávolítja az előfizetés aliasát</span><span class="sxs-lookup"><span data-stu-id="ada85-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="ada85-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ada85-107">EXAMPLES</span></span>

### <span data-ttu-id="ada85-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ada85-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="ada85-109">Az előfizetés aliasának törlése</span><span class="sxs-lookup"><span data-stu-id="ada85-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="ada85-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ada85-110">PARAMETERS</span></span>

### <span data-ttu-id="ada85-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="ada85-111">-AliasName</span></span>
<span data-ttu-id="ada85-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="ada85-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="ada85-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ada85-113">-AsJob</span></span>
<span data-ttu-id="ada85-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ada85-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ada85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada85-115">-DefaultProfile</span></span>
<span data-ttu-id="ada85-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ada85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada85-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ada85-117">-Confirm</span></span>
<span data-ttu-id="ada85-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ada85-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada85-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada85-119">-WhatIf</span></span>
<span data-ttu-id="ada85-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ada85-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada85-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ada85-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada85-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada85-122">CommonParameters</span></span>
<span data-ttu-id="ada85-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada85-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada85-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ada85-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada85-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ada85-125">INPUTS</span></span>

### <span data-ttu-id="ada85-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="ada85-126">None</span></span>

## <span data-ttu-id="ada85-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ada85-127">OUTPUTS</span></span>

### <span data-ttu-id="ada85-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ada85-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="ada85-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ada85-129">NOTES</span></span>

## <span data-ttu-id="ada85-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ada85-130">RELATED LINKS</span></span>
