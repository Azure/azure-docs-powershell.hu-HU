---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149202"
---
# <span data-ttu-id="b7f54-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="b7f54-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="b7f54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f54-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f54-103">Az előfizetéshez rendelkezésre álló consortiums felsorolása.</span><span class="sxs-lookup"><span data-stu-id="b7f54-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="b7f54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7f54-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7f54-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7f54-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f54-106">Az előfizetéshez rendelkezésre álló consortiums felsorolása.</span><span class="sxs-lookup"><span data-stu-id="b7f54-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="b7f54-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7f54-107">EXAMPLES</span></span>

### <span data-ttu-id="b7f54-108">1. példa: Blockchain-consortiumok lekérte.</span><span class="sxs-lookup"><span data-stu-id="b7f54-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="b7f54-109">Ez a parancs felsorolja az adott helyre vonatkozó előfizetés alatt álló consortiumst.</span><span class="sxs-lookup"><span data-stu-id="b7f54-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="b7f54-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7f54-110">PARAMETERS</span></span>

### <span data-ttu-id="b7f54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f54-111">-DefaultProfile</span></span>
<span data-ttu-id="b7f54-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7f54-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f54-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b7f54-113">-Location</span></span>
<span data-ttu-id="b7f54-114">Hely neve.</span><span class="sxs-lookup"><span data-stu-id="b7f54-114">Location Name.</span></span>

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

### <span data-ttu-id="b7f54-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7f54-115">-SubscriptionId</span></span>
<span data-ttu-id="b7f54-116">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="b7f54-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7f54-117">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="b7f54-117">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f54-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7f54-118">-Confirm</span></span>
<span data-ttu-id="b7f54-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7f54-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f54-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f54-120">-WhatIf</span></span>
<span data-ttu-id="b7f54-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7f54-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7f54-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7f54-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f54-123">CommonParameters</span></span>
<span data-ttu-id="b7f54-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f54-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7f54-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f54-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7f54-126">INPUTS</span></span>

## <span data-ttu-id="b7f54-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7f54-127">OUTPUTS</span></span>

### <span data-ttu-id="b7f54-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="b7f54-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="b7f54-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7f54-129">NOTES</span></span>

<span data-ttu-id="b7f54-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b7f54-130">ALIASES</span></span>

## <span data-ttu-id="b7f54-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7f54-131">RELATED LINKS</span></span>

