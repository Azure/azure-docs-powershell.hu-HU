---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195256"
---
# <span data-ttu-id="da0ae-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="da0ae-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="da0ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="da0ae-103">A Transaction Node API-kulcsainak listája</span><span class="sxs-lookup"><span data-stu-id="da0ae-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="da0ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da0ae-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="da0ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da0ae-105">DESCRIPTION</span></span>
<span data-ttu-id="da0ae-106">A Transaction Node API-kulcsainak listája</span><span class="sxs-lookup"><span data-stu-id="da0ae-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="da0ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da0ae-107">EXAMPLES</span></span>

### <span data-ttu-id="da0ae-108">1. példa: egy tranzakciós csomópont List API-kulcsai</span><span class="sxs-lookup"><span data-stu-id="da0ae-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="da0ae-109">Ez a parancs a Transaction csomópont API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="da0ae-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="da0ae-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da0ae-110">PARAMETERS</span></span>

### <span data-ttu-id="da0ae-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="da0ae-111">-BlockchainMemberName</span></span>
<span data-ttu-id="da0ae-112">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="da0ae-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="da0ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0ae-113">-DefaultProfile</span></span>
<span data-ttu-id="da0ae-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da0ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da0ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="da0ae-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da0ae-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="da0ae-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="da0ae-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="da0ae-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da0ae-118">-SubscriptionId</span></span>
<span data-ttu-id="da0ae-119">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="da0ae-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="da0ae-120">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="da0ae-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="da0ae-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="da0ae-121">-TransactionNodeName</span></span>
<span data-ttu-id="da0ae-122">A tranzakció csomópontjának neve</span><span class="sxs-lookup"><span data-stu-id="da0ae-122">Transaction node name.</span></span>

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

### <span data-ttu-id="da0ae-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da0ae-123">-Confirm</span></span>
<span data-ttu-id="da0ae-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da0ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0ae-125">-WhatIf</span></span>
<span data-ttu-id="da0ae-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da0ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da0ae-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da0ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0ae-128">CommonParameters</span></span>
<span data-ttu-id="da0ae-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da0ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0ae-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da0ae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0ae-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da0ae-131">INPUTS</span></span>

## <span data-ttu-id="da0ae-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da0ae-132">OUTPUTS</span></span>

### <span data-ttu-id="da0ae-133">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="da0ae-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="da0ae-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da0ae-134">NOTES</span></span>

<span data-ttu-id="da0ae-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="da0ae-135">ALIASES</span></span>

## <span data-ttu-id="da0ae-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da0ae-136">RELATED LINKS</span></span>

