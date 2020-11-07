---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16649f3f935a488bb6f5913e393f9628e7f26aa7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/22/2020
ms.locfileid: "93506075"
---
# <span data-ttu-id="2b026-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="2b026-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="2b026-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b026-102">SYNOPSIS</span></span>
<span data-ttu-id="2b026-103">Az Azure piactérről letölthető termékek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2b026-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="2b026-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b026-104">SYNTAX</span></span>

### <span data-ttu-id="2b026-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b026-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b026-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="2b026-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="2b026-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b026-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2b026-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b026-108">DESCRIPTION</span></span>
<span data-ttu-id="2b026-109">Az Azure piactérről letölthető termékek listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2b026-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="2b026-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2b026-110">EXAMPLES</span></span>

### <span data-ttu-id="2b026-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b026-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="2b026-112">A rendelkezésre álló termékek listája az Azure piactérről való letöltéshez.</span><span class="sxs-lookup"><span data-stu-id="2b026-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="2b026-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b026-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="2b026-114">Beszerezheti az Azure piactérről való letöltéshez elérhető termékinformációk nevét.</span><span class="sxs-lookup"><span data-stu-id="2b026-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="2b026-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b026-115">PARAMETERS</span></span>

### <span data-ttu-id="2b026-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="2b026-116">-ActivationName</span></span>
<span data-ttu-id="2b026-117">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="2b026-117">Name of the activation.</span></span>

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

### <span data-ttu-id="2b026-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b026-118">-Name</span></span>
<span data-ttu-id="2b026-119">A szorzat neve.</span><span class="sxs-lookup"><span data-stu-id="2b026-119">Name of the product.</span></span>

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

### <span data-ttu-id="2b026-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b026-120">-ResourceGroupName</span></span>
<span data-ttu-id="2b026-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="2b026-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2b026-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b026-122">-ResourceId</span></span>
<span data-ttu-id="2b026-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2b026-123">The resource id.</span></span>

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

### <span data-ttu-id="2b026-124">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2b026-124">-Skip</span></span>
<span data-ttu-id="2b026-125">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="2b026-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2b026-126">-Top</span><span class="sxs-lookup"><span data-stu-id="2b026-126">-Top</span></span>
<span data-ttu-id="2b026-127">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="2b026-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2b026-128">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="2b026-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2b026-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b026-129">CommonParameters</span></span>
<span data-ttu-id="2b026-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b026-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b026-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b026-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b026-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b026-132">INPUTS</span></span>

## <span data-ttu-id="2b026-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b026-133">OUTPUTS</span></span>

### <span data-ttu-id="2b026-134">Microsoft. AzureStack. Management. AzureBridge. admin. models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="2b026-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="2b026-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b026-135">NOTES</span></span>

## <span data-ttu-id="2b026-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b026-136">RELATED LINKS</span></span>

