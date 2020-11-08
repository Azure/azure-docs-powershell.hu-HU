---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025761"
---
# <span data-ttu-id="506c4-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="506c4-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="506c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="506c4-102">SYNOPSIS</span></span>
<span data-ttu-id="506c4-103">Felsorolja az erőforrás típusának SKU-t.</span><span class="sxs-lookup"><span data-stu-id="506c4-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="506c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="506c4-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="506c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="506c4-105">DESCRIPTION</span></span>
<span data-ttu-id="506c4-106">Felsorolja az erőforrás típusának SKU-t.</span><span class="sxs-lookup"><span data-stu-id="506c4-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="506c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="506c4-107">EXAMPLES</span></span>

### <span data-ttu-id="506c4-108">1. példa: előfizetéshez tartozó lista SKU-hoz</span><span class="sxs-lookup"><span data-stu-id="506c4-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="506c4-109">Ez a parancs az előfizetés SKU-ának listáját sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="506c4-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="506c4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="506c4-110">PARAMETERS</span></span>

### <span data-ttu-id="506c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506c4-111">-DefaultProfile</span></span>
<span data-ttu-id="506c4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="506c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="506c4-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="506c4-113">-SubscriptionId</span></span>
<span data-ttu-id="506c4-114">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="506c4-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="506c4-115">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="506c4-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="506c4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506c4-116">CommonParameters</span></span>
<span data-ttu-id="506c4-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="506c4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506c4-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="506c4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506c4-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="506c4-119">INPUTS</span></span>

## <span data-ttu-id="506c4-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="506c4-120">OUTPUTS</span></span>

### <span data-ttu-id="506c4-121">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="506c4-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="506c4-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="506c4-122">NOTES</span></span>

<span data-ttu-id="506c4-123">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="506c4-123">ALIASES</span></span>

## <span data-ttu-id="506c4-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="506c4-124">RELATED LINKS</span></span>

