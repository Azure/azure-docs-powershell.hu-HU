---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840873"
---
# <span data-ttu-id="4888b-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="4888b-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="4888b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4888b-102">SYNOPSIS</span></span>
<span data-ttu-id="4888b-103">A delegatedProviders beszerzése</span><span class="sxs-lookup"><span data-stu-id="4888b-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="4888b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4888b-104">SYNTAX</span></span>

### <span data-ttu-id="4888b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4888b-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="4888b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4888b-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="4888b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4888b-107">DESCRIPTION</span></span>
<span data-ttu-id="4888b-108">A delegatedProviders beszerzése</span><span class="sxs-lookup"><span data-stu-id="4888b-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="4888b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4888b-109">EXAMPLES</span></span>

### <span data-ttu-id="4888b-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4888b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="4888b-111">A delegált szolgáltatók listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4888b-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="4888b-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4888b-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="4888b-113">A megadott meghatalmazott szolgáltató beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4888b-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="4888b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4888b-114">PARAMETERS</span></span>

### <span data-ttu-id="4888b-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="4888b-115">-DelegatedProviderId</span></span>
<span data-ttu-id="4888b-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="4888b-116">{{Fill DelegatedProviderId Description}}</span></span>

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

### <span data-ttu-id="4888b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4888b-117">CommonParameters</span></span>
<span data-ttu-id="4888b-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4888b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4888b-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4888b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4888b-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4888b-120">INPUTS</span></span>

## <span data-ttu-id="4888b-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4888b-121">OUTPUTS</span></span>

### <span data-ttu-id="4888b-122">Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés</span><span class="sxs-lookup"><span data-stu-id="4888b-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="4888b-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4888b-123">NOTES</span></span>

## <span data-ttu-id="4888b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4888b-124">RELATED LINKS</span></span>

