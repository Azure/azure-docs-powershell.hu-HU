---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187978"
---
# <span data-ttu-id="f830e-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="f830e-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="f830e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f830e-102">SYNOPSIS</span></span>
<span data-ttu-id="f830e-103">Az előfizetés aliasnevének részletei</span><span class="sxs-lookup"><span data-stu-id="f830e-103">Gets subscription alias details</span></span>

## <span data-ttu-id="f830e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f830e-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f830e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f830e-105">DESCRIPTION</span></span>
<span data-ttu-id="f830e-106">A **Get-AzSubscriptionAlias** parancsmag az előfizetés aliasnevének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f830e-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="f830e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f830e-107">EXAMPLES</span></span>

### <span data-ttu-id="f830e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f830e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="f830e-109">Az előfizetés aliasnevének részletei</span><span class="sxs-lookup"><span data-stu-id="f830e-109">Gets subscription alias details</span></span>

## <span data-ttu-id="f830e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f830e-110">PARAMETERS</span></span>

### <span data-ttu-id="f830e-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f830e-111">-AliasName</span></span>
<span data-ttu-id="f830e-112">Az előfizetés aliasa</span><span class="sxs-lookup"><span data-stu-id="f830e-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="f830e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f830e-113">-AsJob</span></span>
<span data-ttu-id="f830e-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f830e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f830e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f830e-115">-DefaultProfile</span></span>
<span data-ttu-id="f830e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f830e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f830e-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f830e-117">-Confirm</span></span>
<span data-ttu-id="f830e-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f830e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f830e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f830e-119">-WhatIf</span></span>
<span data-ttu-id="f830e-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f830e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f830e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f830e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f830e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f830e-122">CommonParameters</span></span>
<span data-ttu-id="f830e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f830e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f830e-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f830e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f830e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f830e-125">INPUTS</span></span>

### <span data-ttu-id="f830e-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="f830e-126">None</span></span>

## <span data-ttu-id="f830e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f830e-127">OUTPUTS</span></span>

### <span data-ttu-id="f830e-128">Microsoft. Azure. Command. előfizetés. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f830e-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="f830e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f830e-129">NOTES</span></span>

## <span data-ttu-id="f830e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f830e-130">RELATED LINKS</span></span>
