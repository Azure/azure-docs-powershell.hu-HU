---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840499"
---
# <span data-ttu-id="a251a-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="a251a-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="a251a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a251a-102">SYNOPSIS</span></span>
<span data-ttu-id="a251a-103">Lekérheti az előfizetéses erőforrás-szolgáltatói kvóták listáját egy helyen.</span><span class="sxs-lookup"><span data-stu-id="a251a-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="a251a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a251a-104">SYNTAX</span></span>

### <span data-ttu-id="a251a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a251a-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="a251a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a251a-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="a251a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a251a-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a251a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a251a-108">DESCRIPTION</span></span>
<span data-ttu-id="a251a-109">Letölthet egy helyet a kvóták listájáról.</span><span class="sxs-lookup"><span data-stu-id="a251a-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="a251a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a251a-110">EXAMPLES</span></span>

### <span data-ttu-id="a251a-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a251a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="a251a-112">Lekérheti az előfizetéses erőforrás-szolgáltatói kvóták listáját egy helyen.</span><span class="sxs-lookup"><span data-stu-id="a251a-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="a251a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a251a-113">PARAMETERS</span></span>

### <span data-ttu-id="a251a-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="a251a-114">-Location</span></span>
<span data-ttu-id="a251a-115">A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="a251a-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a251a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a251a-116">-Name</span></span>
<span data-ttu-id="a251a-117">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="a251a-117">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a251a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a251a-118">-ResourceId</span></span>
<span data-ttu-id="a251a-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a251a-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a251a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a251a-120">CommonParameters</span></span>
<span data-ttu-id="a251a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a251a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a251a-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a251a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a251a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a251a-123">INPUTS</span></span>

## <span data-ttu-id="a251a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a251a-124">OUTPUTS</span></span>

### <span data-ttu-id="a251a-125">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. kvóta</span><span class="sxs-lookup"><span data-stu-id="a251a-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="a251a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a251a-126">NOTES</span></span>

## <span data-ttu-id="a251a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a251a-127">RELATED LINKS</span></span>

