---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: 9f33eef5b9f0bd0b245c444cf869fa0ff7a0a064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928354"
---
# <span data-ttu-id="cf449-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="cf449-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="cf449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf449-102">SYNOPSIS</span></span>
<span data-ttu-id="cf449-103">Az erőforrástípushoz szükséges összes lista.</span><span class="sxs-lookup"><span data-stu-id="cf449-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="cf449-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf449-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cf449-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf449-105">DESCRIPTION</span></span>
<span data-ttu-id="cf449-106">Az erőforrástípushoz szükséges összes lista.</span><span class="sxs-lookup"><span data-stu-id="cf449-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="cf449-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf449-107">EXAMPLES</span></span>

### <span data-ttu-id="cf449-108">1. példa: Előfizetés termékváltozatának felsorolása</span><span class="sxs-lookup"><span data-stu-id="cf449-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="cf449-109">Ez a parancs felsorolja az előfizetés termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="cf449-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="cf449-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf449-110">PARAMETERS</span></span>

### <span data-ttu-id="cf449-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf449-111">-DefaultProfile</span></span>
<span data-ttu-id="cf449-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf449-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf449-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf449-113">-SubscriptionId</span></span>
<span data-ttu-id="cf449-114">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="cf449-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf449-115">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="cf449-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf449-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf449-116">CommonParameters</span></span>
<span data-ttu-id="cf449-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf449-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf449-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf449-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf449-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf449-119">INPUTS</span></span>

## <span data-ttu-id="cf449-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf449-120">OUTPUTS</span></span>

### <span data-ttu-id="cf449-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="cf449-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="cf449-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf449-122">NOTES</span></span>

<span data-ttu-id="cf449-123">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cf449-123">ALIASES</span></span>

## <span data-ttu-id="cf449-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf449-124">RELATED LINKS</span></span>

