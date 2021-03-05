---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: 2dd2ec778a64403b9f13cd923e7b7312e72a6c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003813"
---
# <span data-ttu-id="79d00-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="79d00-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="79d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d00-102">SYNOPSIS</span></span>
<span data-ttu-id="79d00-103">Privát áruházak listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="79d00-103">Get private store list</span></span>

## <span data-ttu-id="79d00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79d00-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79d00-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79d00-105">DESCRIPTION</span></span>
<span data-ttu-id="79d00-106">Bérlői hatókör alatt létrehozott privát áruházlista lekérte</span><span class="sxs-lookup"><span data-stu-id="79d00-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="79d00-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79d00-107">EXAMPLES</span></span>

### <span data-ttu-id="79d00-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="79d00-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="79d00-109">a bérlői hatókör alatt létrehozott privát áruházak listája</span><span class="sxs-lookup"><span data-stu-id="79d00-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="79d00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79d00-110">PARAMETERS</span></span>

### <span data-ttu-id="79d00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d00-111">-DefaultProfile</span></span>
<span data-ttu-id="79d00-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79d00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d00-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d00-113">CommonParameters</span></span>
<span data-ttu-id="79d00-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d00-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d00-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79d00-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d00-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79d00-116">INPUTS</span></span>

### <span data-ttu-id="79d00-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="79d00-117">None</span></span>

## <span data-ttu-id="79d00-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79d00-118">OUTPUTS</span></span>

### <span data-ttu-id="79d00-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="79d00-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="79d00-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79d00-120">NOTES</span></span>

## <span data-ttu-id="79d00-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79d00-121">RELATED LINKS</span></span>
