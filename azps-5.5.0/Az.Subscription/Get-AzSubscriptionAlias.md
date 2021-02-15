---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150114"
---
# <span data-ttu-id="c6c7a-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="c6c7a-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="c6c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c7a-103">Előfizetési alias részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="c6c7a-103">Gets subscription alias details</span></span>

## <span data-ttu-id="c6c7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c6c7a-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6c7a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c6c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c7a-106">A **Get-AzSubscriptionAlias** parancsmag megkapja az előfizetés aliasának részleteit.</span><span class="sxs-lookup"><span data-stu-id="c6c7a-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="c6c7a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c6c7a-107">EXAMPLES</span></span>

### <span data-ttu-id="c6c7a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c6c7a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="c6c7a-109">Előfizetési alias részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="c6c7a-109">Gets subscription alias details</span></span>

## <span data-ttu-id="c6c7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6c7a-110">PARAMETERS</span></span>

### <span data-ttu-id="c6c7a-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="c6c7a-111">-AliasName</span></span>
<span data-ttu-id="c6c7a-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="c6c7a-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="c6c7a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6c7a-113">-AsJob</span></span>
<span data-ttu-id="c6c7a-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c6c7a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6c7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c7a-115">-DefaultProfile</span></span>
<span data-ttu-id="c6c7a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6c7a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c7a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6c7a-117">-Confirm</span></span>
<span data-ttu-id="c6c7a-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c6c7a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6c7a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6c7a-119">-WhatIf</span></span>
<span data-ttu-id="c6c7a-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c6c7a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6c7a-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6c7a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6c7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c7a-122">CommonParameters</span></span>
<span data-ttu-id="c6c7a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c7a-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6c7a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c7a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6c7a-125">INPUTS</span></span>

### <span data-ttu-id="c6c7a-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="c6c7a-126">None</span></span>

## <span data-ttu-id="c6c7a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c7a-127">OUTPUTS</span></span>

### <span data-ttu-id="c6c7a-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c6c7a-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="c6c7a-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c6c7a-129">NOTES</span></span>

## <span data-ttu-id="c6c7a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6c7a-130">RELATED LINKS</span></span>
