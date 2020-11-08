---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1780eeb2f5d03fafd056c7987f648eae989b3dd
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/22/2020
ms.locfileid: "94185132"
---
# <span data-ttu-id="72a7c-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="72a7c-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="72a7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="72a7c-103">Az Azure piactérről letöltött termékek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="72a7c-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="72a7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72a7c-104">SYNTAX</span></span>

### <span data-ttu-id="72a7c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72a7c-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="72a7c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="72a7c-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="72a7c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="72a7c-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="72a7c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="72a7c-108">DESCRIPTION</span></span>
<span data-ttu-id="72a7c-109">Az Azure piactérről letöltött termékek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="72a7c-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="72a7c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="72a7c-110">EXAMPLES</span></span>

### <span data-ttu-id="72a7c-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="72a7c-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="72a7c-112">Az Azure Bridge letöltött termékeinek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="72a7c-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="72a7c-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="72a7c-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="72a7c-114">Az Azure Bridge letölthető termékek beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="72a7c-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="72a7c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72a7c-115">PARAMETERS</span></span>

### <span data-ttu-id="72a7c-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72a7c-116">-Name</span></span>
<span data-ttu-id="72a7c-117">A szorzat neve.</span><span class="sxs-lookup"><span data-stu-id="72a7c-117">Name of the product.</span></span>

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

### <span data-ttu-id="72a7c-118">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="72a7c-118">-ActivationName</span></span>
<span data-ttu-id="72a7c-119">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="72a7c-119">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="72a7c-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="72a7c-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a7c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72a7c-122">-ResourceId</span></span>
<span data-ttu-id="72a7c-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="72a7c-123">The resource id.</span></span>

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

### <span data-ttu-id="72a7c-124">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="72a7c-124">-Skip</span></span>
<span data-ttu-id="72a7c-125">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="72a7c-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a7c-126">-Top</span><span class="sxs-lookup"><span data-stu-id="72a7c-126">-Top</span></span>
<span data-ttu-id="72a7c-127">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="72a7c-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="72a7c-128">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="72a7c-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a7c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a7c-129">CommonParameters</span></span>
<span data-ttu-id="72a7c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72a7c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a7c-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a7c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a7c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72a7c-132">INPUTS</span></span>

## <span data-ttu-id="72a7c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72a7c-133">OUTPUTS</span></span>

### <span data-ttu-id="72a7c-134">Microsoft. AzureStack. Management. AzureBridge. admin. models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="72a7c-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="72a7c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72a7c-135">NOTES</span></span>

## <span data-ttu-id="72a7c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72a7c-136">RELATED LINKS</span></span>