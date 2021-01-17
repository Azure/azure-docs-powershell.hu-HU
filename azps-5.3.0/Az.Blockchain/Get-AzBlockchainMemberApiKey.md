---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478114"
---
# <span data-ttu-id="a3923-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="a3923-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="a3923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3923-102">SYNOPSIS</span></span>
<span data-ttu-id="a3923-103">A blockchain-tag API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="a3923-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="a3923-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3923-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3923-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3923-105">DESCRIPTION</span></span>
<span data-ttu-id="a3923-106">A blockchain-tag API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="a3923-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="a3923-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3923-107">EXAMPLES</span></span>

### <span data-ttu-id="a3923-108">1. példa: A blockchain Api-kulcsok listája</span><span class="sxs-lookup"><span data-stu-id="a3923-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="a3923-109">Ez a parancs felsorolja egy blockchain-tag API-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="a3923-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="a3923-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3923-110">PARAMETERS</span></span>

### <span data-ttu-id="a3923-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="a3923-111">-BlockchainMemberName</span></span>
<span data-ttu-id="a3923-112">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="a3923-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="a3923-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3923-113">-DefaultProfile</span></span>
<span data-ttu-id="a3923-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3923-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3923-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3923-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3923-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a3923-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a3923-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="a3923-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a3923-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3923-118">-SubscriptionId</span></span>
<span data-ttu-id="a3923-119">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="a3923-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a3923-120">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="a3923-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a3923-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3923-121">-Confirm</span></span>
<span data-ttu-id="a3923-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a3923-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3923-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3923-123">-WhatIf</span></span>
<span data-ttu-id="a3923-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a3923-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3923-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3923-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3923-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3923-126">CommonParameters</span></span>
<span data-ttu-id="a3923-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3923-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3923-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3923-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3923-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3923-129">INPUTS</span></span>

## <span data-ttu-id="a3923-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3923-130">OUTPUTS</span></span>

### <span data-ttu-id="a3923-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="a3923-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="a3923-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3923-132">NOTES</span></span>

<span data-ttu-id="a3923-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a3923-133">ALIASES</span></span>

## <span data-ttu-id="a3923-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3923-134">RELATED LINKS</span></span>

