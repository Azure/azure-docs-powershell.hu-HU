---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: 0cce48f38b669c713f0d3a193deec64cfce649e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937265"
---
# <span data-ttu-id="b5dec-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="b5dec-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="b5dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5dec-102">SYNOPSIS</span></span>
<span data-ttu-id="b5dec-103">Előfizetési alias részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="b5dec-103">Gets subscription alias details</span></span>

## <span data-ttu-id="b5dec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5dec-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5dec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5dec-105">DESCRIPTION</span></span>
<span data-ttu-id="b5dec-106">A **Get-AzSubscriptionAlias** parancsmag megkapja az előfizetés aliasának részleteit.</span><span class="sxs-lookup"><span data-stu-id="b5dec-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="b5dec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5dec-107">EXAMPLES</span></span>

### <span data-ttu-id="b5dec-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b5dec-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="b5dec-109">Előfizetési alias részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="b5dec-109">Gets subscription alias details</span></span>

## <span data-ttu-id="b5dec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5dec-110">PARAMETERS</span></span>

### <span data-ttu-id="b5dec-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="b5dec-111">-AliasName</span></span>
<span data-ttu-id="b5dec-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="b5dec-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="b5dec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5dec-113">-AsJob</span></span>
<span data-ttu-id="b5dec-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b5dec-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5dec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5dec-115">-DefaultProfile</span></span>
<span data-ttu-id="b5dec-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5dec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5dec-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5dec-117">-Confirm</span></span>
<span data-ttu-id="b5dec-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b5dec-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5dec-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5dec-119">-WhatIf</span></span>
<span data-ttu-id="b5dec-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b5dec-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5dec-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5dec-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5dec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5dec-122">CommonParameters</span></span>
<span data-ttu-id="b5dec-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5dec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5dec-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5dec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5dec-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5dec-125">INPUTS</span></span>

### <span data-ttu-id="b5dec-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5dec-126">None</span></span>

## <span data-ttu-id="b5dec-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5dec-127">OUTPUTS</span></span>

### <span data-ttu-id="b5dec-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b5dec-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="b5dec-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5dec-129">NOTES</span></span>

## <span data-ttu-id="b5dec-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5dec-130">RELATED LINKS</span></span>
