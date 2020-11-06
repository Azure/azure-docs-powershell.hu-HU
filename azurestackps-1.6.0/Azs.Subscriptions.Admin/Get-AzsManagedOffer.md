---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491528"
---
# <span data-ttu-id="2f06e-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="2f06e-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="2f06e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f06e-102">SYNOPSIS</span></span>
<span data-ttu-id="2f06e-103">Az ajánlatok listájának beszerzése operátorként.</span><span class="sxs-lookup"><span data-stu-id="2f06e-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="2f06e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f06e-104">SYNTAX</span></span>

### <span data-ttu-id="2f06e-105">ListAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f06e-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2f06e-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f06e-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="2f06e-107">Lista</span><span class="sxs-lookup"><span data-stu-id="2f06e-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2f06e-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f06e-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2f06e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f06e-109">DESCRIPTION</span></span>
<span data-ttu-id="2f06e-110">Az ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f06e-110">Get the list of offers.</span></span>

## <span data-ttu-id="2f06e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2f06e-111">EXAMPLES</span></span>

### <span data-ttu-id="2f06e-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f06e-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="2f06e-113">Az ajánlatok listájának beszerzése operátorként.</span><span class="sxs-lookup"><span data-stu-id="2f06e-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="2f06e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f06e-114">PARAMETERS</span></span>

### <span data-ttu-id="2f06e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f06e-115">-Name</span></span>
<span data-ttu-id="2f06e-116">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="2f06e-116">Name of an offer.</span></span>

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

### <span data-ttu-id="2f06e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f06e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f06e-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="2f06e-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f06e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f06e-119">-ResourceId</span></span>
<span data-ttu-id="2f06e-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2f06e-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f06e-121">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2f06e-121">-Skip</span></span>
<span data-ttu-id="2f06e-122">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="2f06e-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f06e-123">-Top</span><span class="sxs-lookup"><span data-stu-id="2f06e-123">-Top</span></span>
<span data-ttu-id="2f06e-124">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="2f06e-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2f06e-125">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="2f06e-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f06e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f06e-126">CommonParameters</span></span>
<span data-ttu-id="2f06e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f06e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f06e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f06e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f06e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f06e-129">INPUTS</span></span>

## <span data-ttu-id="2f06e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f06e-130">OUTPUTS</span></span>

### <span data-ttu-id="2f06e-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="2f06e-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="2f06e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f06e-132">NOTES</span></span>

## <span data-ttu-id="2f06e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f06e-133">RELATED LINKS</span></span>

