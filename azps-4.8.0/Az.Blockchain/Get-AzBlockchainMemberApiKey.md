---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017901"
---
# <span data-ttu-id="37b89-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="37b89-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="37b89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37b89-102">SYNOPSIS</span></span>
<span data-ttu-id="37b89-103">A blockchain-tagok API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="37b89-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="37b89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37b89-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37b89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37b89-105">DESCRIPTION</span></span>
<span data-ttu-id="37b89-106">A blockchain-tagok API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="37b89-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="37b89-107">Példák</span><span class="sxs-lookup"><span data-stu-id="37b89-107">EXAMPLES</span></span>

### <span data-ttu-id="37b89-108">1. példa: a lista blockchain API-kulcsai</span><span class="sxs-lookup"><span data-stu-id="37b89-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="37b89-109">Ez a parancs az blockchain-tagok API-kulcsait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="37b89-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="37b89-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37b89-110">PARAMETERS</span></span>

### <span data-ttu-id="37b89-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="37b89-111">-BlockchainMemberName</span></span>
<span data-ttu-id="37b89-112">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="37b89-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="37b89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b89-113">-DefaultProfile</span></span>
<span data-ttu-id="37b89-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37b89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b89-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b89-115">-ResourceGroupName</span></span>
<span data-ttu-id="37b89-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="37b89-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="37b89-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="37b89-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="37b89-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37b89-118">-SubscriptionId</span></span>
<span data-ttu-id="37b89-119">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="37b89-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="37b89-120">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="37b89-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37b89-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="37b89-121">-Confirm</span></span>
<span data-ttu-id="37b89-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="37b89-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b89-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b89-123">-WhatIf</span></span>
<span data-ttu-id="37b89-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="37b89-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b89-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37b89-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b89-126">CommonParameters</span></span>
<span data-ttu-id="37b89-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37b89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b89-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="37b89-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b89-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37b89-129">INPUTS</span></span>

## <span data-ttu-id="37b89-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37b89-130">OUTPUTS</span></span>

### <span data-ttu-id="37b89-131">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="37b89-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="37b89-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37b89-132">NOTES</span></span>

<span data-ttu-id="37b89-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="37b89-133">ALIASES</span></span>

## <span data-ttu-id="37b89-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37b89-134">RELATED LINKS</span></span>

