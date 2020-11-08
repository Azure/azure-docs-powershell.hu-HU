---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/22/2020
ms.locfileid: "94185130"
---
# <span data-ttu-id="cedb0-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="cedb0-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="cedb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cedb0-102">SYNOPSIS</span></span>
<span data-ttu-id="cedb0-103">Az Azure piactérről letölthető termékek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="cedb0-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="cedb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cedb0-104">SYNTAX</span></span>

### <span data-ttu-id="cedb0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cedb0-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cedb0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="cedb0-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="cedb0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cedb0-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cedb0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cedb0-108">DESCRIPTION</span></span>
<span data-ttu-id="cedb0-109">Az Azure piactérről letölthető termékek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="cedb0-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="cedb0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cedb0-110">EXAMPLES</span></span>

### <span data-ttu-id="cedb0-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="cedb0-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="cedb0-112">A rendelkezésre álló termékek listája az Azure piactérről való letöltéshez.</span><span class="sxs-lookup"><span data-stu-id="cedb0-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="cedb0-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="cedb0-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="cedb0-114">Beszerezheti az Azure piactérről való letöltéshez elérhető termékinformációk nevét.</span><span class="sxs-lookup"><span data-stu-id="cedb0-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="cedb0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cedb0-115">PARAMETERS</span></span>

### <span data-ttu-id="cedb0-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cedb0-116">-Name</span></span>
<span data-ttu-id="cedb0-117">A szorzat neve.</span><span class="sxs-lookup"><span data-stu-id="cedb0-117">Name of the product.</span></span>

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

### <span data-ttu-id="cedb0-118">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="cedb0-118">-ActivationName</span></span>
<span data-ttu-id="cedb0-119">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="cedb0-119">Name of the activation.</span></span>

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

### <span data-ttu-id="cedb0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cedb0-120">-ResourceGroupName</span></span>
<span data-ttu-id="cedb0-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="cedb0-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="cedb0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cedb0-122">-ResourceId</span></span>
<span data-ttu-id="cedb0-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cedb0-123">The resource id.</span></span>

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

### <span data-ttu-id="cedb0-124">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="cedb0-124">-Skip</span></span>
<span data-ttu-id="cedb0-125">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="cedb0-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cedb0-126">-Top</span><span class="sxs-lookup"><span data-stu-id="cedb0-126">-Top</span></span>
<span data-ttu-id="cedb0-127">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="cedb0-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cedb0-128">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="cedb0-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cedb0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cedb0-129">CommonParameters</span></span>
<span data-ttu-id="cedb0-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cedb0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cedb0-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cedb0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cedb0-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cedb0-132">INPUTS</span></span>

## <span data-ttu-id="cedb0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cedb0-133">OUTPUTS</span></span>

### <span data-ttu-id="cedb0-134">Microsoft. AzureStack. Management. AzureBridge. admin. models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="cedb0-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="cedb0-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cedb0-135">NOTES</span></span>

## <span data-ttu-id="cedb0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cedb0-136">RELATED LINKS</span></span>
