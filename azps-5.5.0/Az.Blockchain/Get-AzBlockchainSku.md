---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162427"
---
# <span data-ttu-id="108fd-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="108fd-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="108fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="108fd-102">SYNOPSIS</span></span>
<span data-ttu-id="108fd-103">Az erőforrástípushoz szükséges összes lista.</span><span class="sxs-lookup"><span data-stu-id="108fd-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="108fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="108fd-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="108fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="108fd-105">DESCRIPTION</span></span>
<span data-ttu-id="108fd-106">Az erőforrástípushoz szükséges összes lista.</span><span class="sxs-lookup"><span data-stu-id="108fd-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="108fd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="108fd-107">EXAMPLES</span></span>

### <span data-ttu-id="108fd-108">1. példa: Előfizetés termékváltozatának felsorolása</span><span class="sxs-lookup"><span data-stu-id="108fd-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="108fd-109">Ez a parancs felsorolja az előfizetés termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="108fd-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="108fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="108fd-110">PARAMETERS</span></span>

### <span data-ttu-id="108fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108fd-111">-DefaultProfile</span></span>
<span data-ttu-id="108fd-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="108fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="108fd-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="108fd-113">-SubscriptionId</span></span>
<span data-ttu-id="108fd-114">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="108fd-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="108fd-115">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="108fd-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="108fd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108fd-116">CommonParameters</span></span>
<span data-ttu-id="108fd-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108fd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108fd-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="108fd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108fd-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="108fd-119">INPUTS</span></span>

## <span data-ttu-id="108fd-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="108fd-120">OUTPUTS</span></span>

### <span data-ttu-id="108fd-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="108fd-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="108fd-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="108fd-122">NOTES</span></span>

<span data-ttu-id="108fd-123">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="108fd-123">ALIASES</span></span>

## <span data-ttu-id="108fd-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="108fd-124">RELATED LINKS</span></span>

