---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333125"
---
# <span data-ttu-id="1e766-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="1e766-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="1e766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e766-102">SYNOPSIS</span></span>
<span data-ttu-id="1e766-103">Az előfizetéshez rendelkezésre álló consortiums felsorolása.</span><span class="sxs-lookup"><span data-stu-id="1e766-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="1e766-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e766-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e766-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e766-105">DESCRIPTION</span></span>
<span data-ttu-id="1e766-106">Az előfizetéshez rendelkezésre álló consortiums felsorolása.</span><span class="sxs-lookup"><span data-stu-id="1e766-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="1e766-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e766-107">EXAMPLES</span></span>

### <span data-ttu-id="1e766-108">1. példa: Blockchain-consortiumok lekérte.</span><span class="sxs-lookup"><span data-stu-id="1e766-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="1e766-109">Ez a parancs felsorolja az adott helyre vonatkozó előfizetés alatt álló consortiumst.</span><span class="sxs-lookup"><span data-stu-id="1e766-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="1e766-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e766-110">PARAMETERS</span></span>

### <span data-ttu-id="1e766-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e766-111">-DefaultProfile</span></span>
<span data-ttu-id="1e766-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e766-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e766-113">-Location</span><span class="sxs-lookup"><span data-stu-id="1e766-113">-Location</span></span>
<span data-ttu-id="1e766-114">Hely neve.</span><span class="sxs-lookup"><span data-stu-id="1e766-114">Location Name.</span></span>

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

### <span data-ttu-id="1e766-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e766-115">-SubscriptionId</span></span>
<span data-ttu-id="1e766-116">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="1e766-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e766-117">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="1e766-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1e766-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e766-118">-Confirm</span></span>
<span data-ttu-id="1e766-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1e766-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e766-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e766-120">-WhatIf</span></span>
<span data-ttu-id="1e766-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1e766-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e766-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e766-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e766-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e766-123">CommonParameters</span></span>
<span data-ttu-id="1e766-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e766-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e766-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e766-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e766-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e766-126">INPUTS</span></span>

## <span data-ttu-id="1e766-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e766-127">OUTPUTS</span></span>

### <span data-ttu-id="1e766-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="1e766-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="1e766-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e766-129">NOTES</span></span>

<span data-ttu-id="1e766-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1e766-130">ALIASES</span></span>

## <span data-ttu-id="1e766-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e766-131">RELATED LINKS</span></span>

