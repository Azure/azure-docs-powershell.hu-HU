---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: dbde273c1694f4622904ac00b261e902036c6e03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928345"
---
# <span data-ttu-id="d4e02-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="d4e02-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="d4e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e02-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e02-103">Sorolja fel a tranzakciós csomópont API-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="d4e02-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="d4e02-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4e02-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d4e02-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4e02-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e02-106">Sorolja fel a tranzakciós csomópont API-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="d4e02-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="d4e02-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4e02-107">EXAMPLES</span></span>

### <span data-ttu-id="d4e02-108">1. példa: A tranzakciós csomópont Api-billentyűinek felsorolása</span><span class="sxs-lookup"><span data-stu-id="d4e02-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="d4e02-109">Ez a parancs felsorolja egy tranzakciós csomópont Api-kulcsait.</span><span class="sxs-lookup"><span data-stu-id="d4e02-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="d4e02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4e02-110">PARAMETERS</span></span>

### <span data-ttu-id="d4e02-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="d4e02-111">-BlockchainMemberName</span></span>
<span data-ttu-id="d4e02-112">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="d4e02-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="d4e02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e02-113">-DefaultProfile</span></span>
<span data-ttu-id="d4e02-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4e02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e02-115">-ResourceGroupName</span></span>
<span data-ttu-id="d4e02-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4e02-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d4e02-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="d4e02-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d4e02-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4e02-118">-SubscriptionId</span></span>
<span data-ttu-id="d4e02-119">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="d4e02-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4e02-120">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="d4e02-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4e02-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="d4e02-121">-TransactionNodeName</span></span>
<span data-ttu-id="d4e02-122">Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="d4e02-122">Transaction node name.</span></span>

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

### <span data-ttu-id="d4e02-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4e02-123">-Confirm</span></span>
<span data-ttu-id="d4e02-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4e02-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e02-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e02-125">-WhatIf</span></span>
<span data-ttu-id="d4e02-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4e02-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e02-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4e02-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e02-128">CommonParameters</span></span>
<span data-ttu-id="d4e02-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e02-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4e02-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e02-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4e02-131">INPUTS</span></span>

## <span data-ttu-id="d4e02-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4e02-132">OUTPUTS</span></span>

### <span data-ttu-id="d4e02-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="d4e02-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="d4e02-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4e02-134">NOTES</span></span>

<span data-ttu-id="d4e02-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d4e02-135">ALIASES</span></span>

## <span data-ttu-id="d4e02-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4e02-136">RELATED LINKS</span></span>

