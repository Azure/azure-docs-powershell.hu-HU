---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016826"
---
# <span data-ttu-id="6fa9a-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="6fa9a-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="6fa9a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fa9a-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa9a-103">Az ajánlatok listájának beszerzése rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="6fa9a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fa9a-104">SYNTAX</span></span>

### <span data-ttu-id="6fa9a-105">ListAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fa9a-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6fa9a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6fa9a-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="6fa9a-107">Lista</span><span class="sxs-lookup"><span data-stu-id="6fa9a-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6fa9a-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fa9a-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6fa9a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fa9a-109">DESCRIPTION</span></span>
<span data-ttu-id="6fa9a-110">Az ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="6fa9a-110">Get the list of offers.</span></span>

## <span data-ttu-id="6fa9a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6fa9a-111">EXAMPLES</span></span>

### <span data-ttu-id="6fa9a-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6fa9a-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="6fa9a-113">Az ajánlatok listájának beszerzése rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="6fa9a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fa9a-114">PARAMETERS</span></span>

### <span data-ttu-id="6fa9a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6fa9a-115">-Name</span></span>
<span data-ttu-id="6fa9a-116">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-116">Name of an offer.</span></span>

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

### <span data-ttu-id="6fa9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fa9a-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6fa9a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fa9a-119">-ResourceId</span></span>
<span data-ttu-id="6fa9a-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-120">The resource id.</span></span>

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

### <span data-ttu-id="6fa9a-121">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6fa9a-121">-Skip</span></span>
<span data-ttu-id="6fa9a-122">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6fa9a-123">-Top</span><span class="sxs-lookup"><span data-stu-id="6fa9a-123">-Top</span></span>
<span data-ttu-id="6fa9a-124">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6fa9a-125">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="6fa9a-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6fa9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa9a-126">CommonParameters</span></span>
<span data-ttu-id="6fa9a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fa9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa9a-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa9a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa9a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fa9a-129">INPUTS</span></span>

## <span data-ttu-id="6fa9a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fa9a-130">OUTPUTS</span></span>

### <span data-ttu-id="6fa9a-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="6fa9a-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="6fa9a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fa9a-132">NOTES</span></span>

## <span data-ttu-id="6fa9a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fa9a-133">RELATED LINKS</span></span>

