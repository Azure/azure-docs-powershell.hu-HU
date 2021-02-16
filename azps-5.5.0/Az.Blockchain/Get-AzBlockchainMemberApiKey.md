---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145194"
---
# <span data-ttu-id="402ad-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="402ad-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="402ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="402ad-102">SYNOPSIS</span></span>
<span data-ttu-id="402ad-103">A blockchain-tag API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="402ad-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="402ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="402ad-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="402ad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="402ad-105">DESCRIPTION</span></span>
<span data-ttu-id="402ad-106">A blockchain-tag API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="402ad-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="402ad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="402ad-107">EXAMPLES</span></span>

### <span data-ttu-id="402ad-108">1. példa: A blockchain Api-kulcsok listája</span><span class="sxs-lookup"><span data-stu-id="402ad-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="402ad-109">Ez a parancs felsorolja egy blockchain-tag API-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="402ad-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="402ad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="402ad-110">PARAMETERS</span></span>

### <span data-ttu-id="402ad-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="402ad-111">-BlockchainMemberName</span></span>
<span data-ttu-id="402ad-112">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="402ad-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="402ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402ad-113">-DefaultProfile</span></span>
<span data-ttu-id="402ad-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="402ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="402ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="402ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="402ad-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="402ad-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="402ad-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="402ad-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="402ad-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="402ad-118">-SubscriptionId</span></span>
<span data-ttu-id="402ad-119">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="402ad-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="402ad-120">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="402ad-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="402ad-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="402ad-121">-Confirm</span></span>
<span data-ttu-id="402ad-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="402ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402ad-123">-WhatIf</span></span>
<span data-ttu-id="402ad-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="402ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="402ad-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="402ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402ad-126">CommonParameters</span></span>
<span data-ttu-id="402ad-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402ad-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="402ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402ad-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="402ad-129">INPUTS</span></span>

## <span data-ttu-id="402ad-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="402ad-130">OUTPUTS</span></span>

### <span data-ttu-id="402ad-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="402ad-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="402ad-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="402ad-132">NOTES</span></span>

<span data-ttu-id="402ad-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="402ad-133">ALIASES</span></span>

## <span data-ttu-id="402ad-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="402ad-134">RELATED LINKS</span></span>

