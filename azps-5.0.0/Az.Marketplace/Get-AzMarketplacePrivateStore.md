---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194349"
---
# <span data-ttu-id="3c91d-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="3c91d-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="3c91d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c91d-102">SYNOPSIS</span></span>
<span data-ttu-id="3c91d-103">Privát áruházi lista beszerzése</span><span class="sxs-lookup"><span data-stu-id="3c91d-103">Get private store list</span></span>

## <span data-ttu-id="3c91d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c91d-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c91d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c91d-105">DESCRIPTION</span></span>
<span data-ttu-id="3c91d-106">A bérlői hatókör csoportban létrehozott magánjellegű áruházból álló lista beszerzése</span><span class="sxs-lookup"><span data-stu-id="3c91d-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="3c91d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c91d-107">EXAMPLES</span></span>

### <span data-ttu-id="3c91d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3c91d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="3c91d-109">a bérlői hatókör csoportban létrehozott privát áruház lista</span><span class="sxs-lookup"><span data-stu-id="3c91d-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="3c91d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c91d-110">PARAMETERS</span></span>

### <span data-ttu-id="3c91d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c91d-111">-DefaultProfile</span></span>
<span data-ttu-id="3c91d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c91d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c91d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c91d-113">CommonParameters</span></span>
<span data-ttu-id="3c91d-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c91d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c91d-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c91d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c91d-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c91d-116">INPUTS</span></span>

### <span data-ttu-id="3c91d-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="3c91d-117">None</span></span>

## <span data-ttu-id="3c91d-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c91d-118">OUTPUTS</span></span>

### <span data-ttu-id="3c91d-119">Microsoft. Azure. Command. Marketplace. models. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="3c91d-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="3c91d-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c91d-120">NOTES</span></span>

## <span data-ttu-id="3c91d-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c91d-121">RELATED LINKS</span></span>
