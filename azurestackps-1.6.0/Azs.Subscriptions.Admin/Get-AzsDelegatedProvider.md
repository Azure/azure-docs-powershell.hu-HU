---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491568"
---
# <span data-ttu-id="e43f3-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="e43f3-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="e43f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e43f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e43f3-103">A delegatedProviders beszerzése</span><span class="sxs-lookup"><span data-stu-id="e43f3-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="e43f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e43f3-104">SYNTAX</span></span>

### <span data-ttu-id="e43f3-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e43f3-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="e43f3-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e43f3-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="e43f3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e43f3-107">DESCRIPTION</span></span>
<span data-ttu-id="e43f3-108">A delegatedProviders beszerzése</span><span class="sxs-lookup"><span data-stu-id="e43f3-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="e43f3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e43f3-109">EXAMPLES</span></span>

### <span data-ttu-id="e43f3-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e43f3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="e43f3-111">A delegált szolgáltatók listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e43f3-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="e43f3-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e43f3-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e43f3-113">A megadott meghatalmazott szolgáltató beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e43f3-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="e43f3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e43f3-114">PARAMETERS</span></span>

### <span data-ttu-id="e43f3-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="e43f3-115">-DelegatedProviderId</span></span>
<span data-ttu-id="e43f3-116">DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e43f3-116">DelegatedProvider identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43f3-117">CommonParameters</span></span>
<span data-ttu-id="e43f3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e43f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43f3-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e43f3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43f3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e43f3-120">INPUTS</span></span>

## <span data-ttu-id="e43f3-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e43f3-121">OUTPUTS</span></span>

### <span data-ttu-id="e43f3-122">Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés</span><span class="sxs-lookup"><span data-stu-id="e43f3-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="e43f3-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e43f3-123">NOTES</span></span>

## <span data-ttu-id="e43f3-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e43f3-124">RELATED LINKS</span></span>

