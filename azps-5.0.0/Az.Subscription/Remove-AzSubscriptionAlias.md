---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187973"
---
# <span data-ttu-id="5a75e-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="5a75e-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="5a75e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a75e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a75e-103">Az előfizetés aliasnevének törlése</span><span class="sxs-lookup"><span data-stu-id="5a75e-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="5a75e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a75e-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a75e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a75e-105">DESCRIPTION</span></span>
<span data-ttu-id="5a75e-106">A **Remove-AzSubscriptionAlias** parancsmag eltávolítja az előfizetés aliasnevét</span><span class="sxs-lookup"><span data-stu-id="5a75e-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="5a75e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5a75e-107">EXAMPLES</span></span>

### <span data-ttu-id="5a75e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a75e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="5a75e-109">Az előfizetés aliasnevének törlése</span><span class="sxs-lookup"><span data-stu-id="5a75e-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="5a75e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a75e-110">PARAMETERS</span></span>

### <span data-ttu-id="5a75e-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="5a75e-111">-AliasName</span></span>
<span data-ttu-id="5a75e-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="5a75e-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="5a75e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a75e-113">-AsJob</span></span>
<span data-ttu-id="5a75e-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5a75e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a75e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a75e-115">-DefaultProfile</span></span>
<span data-ttu-id="5a75e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a75e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a75e-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a75e-117">-Confirm</span></span>
<span data-ttu-id="5a75e-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a75e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a75e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a75e-119">-WhatIf</span></span>
<span data-ttu-id="5a75e-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a75e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a75e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a75e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a75e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a75e-122">CommonParameters</span></span>
<span data-ttu-id="5a75e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a75e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a75e-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a75e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a75e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a75e-125">INPUTS</span></span>

### <span data-ttu-id="5a75e-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="5a75e-126">None</span></span>

## <span data-ttu-id="5a75e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a75e-127">OUTPUTS</span></span>

### <span data-ttu-id="5a75e-128">Microsoft. Azure. Command. előfizetés. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="5a75e-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="5a75e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a75e-129">NOTES</span></span>

## <span data-ttu-id="5a75e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a75e-130">RELATED LINKS</span></span>
