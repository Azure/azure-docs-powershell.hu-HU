---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024196"
---
# <span data-ttu-id="05069-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="05069-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="05069-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05069-102">SYNOPSIS</span></span>
<span data-ttu-id="05069-103">Az előfizetéshez elérhető konzorciumokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="05069-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="05069-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05069-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05069-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05069-105">DESCRIPTION</span></span>
<span data-ttu-id="05069-106">Az előfizetéshez elérhető konzorciumokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="05069-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="05069-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05069-107">EXAMPLES</span></span>

### <span data-ttu-id="05069-108">1. példa: Blockchain-konzorciumok beszerzése</span><span class="sxs-lookup"><span data-stu-id="05069-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="05069-109">Ez a parancs felsorolja a konzorciumokat egy adott helyre szóló előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="05069-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="05069-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05069-110">PARAMETERS</span></span>

### <span data-ttu-id="05069-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05069-111">-DefaultProfile</span></span>
<span data-ttu-id="05069-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05069-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05069-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="05069-113">-Location</span></span>
<span data-ttu-id="05069-114">Tartózkodási hely neve.</span><span class="sxs-lookup"><span data-stu-id="05069-114">Location Name.</span></span>

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

### <span data-ttu-id="05069-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05069-115">-SubscriptionId</span></span>
<span data-ttu-id="05069-116">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="05069-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="05069-117">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="05069-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="05069-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05069-118">-Confirm</span></span>
<span data-ttu-id="05069-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05069-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05069-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05069-120">-WhatIf</span></span>
<span data-ttu-id="05069-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05069-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05069-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05069-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05069-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05069-123">CommonParameters</span></span>
<span data-ttu-id="05069-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05069-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05069-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05069-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05069-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05069-126">INPUTS</span></span>

## <span data-ttu-id="05069-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05069-127">OUTPUTS</span></span>

### <span data-ttu-id="05069-128">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="05069-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="05069-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05069-129">NOTES</span></span>

<span data-ttu-id="05069-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="05069-130">ALIASES</span></span>

## <span data-ttu-id="05069-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05069-131">RELATED LINKS</span></span>

