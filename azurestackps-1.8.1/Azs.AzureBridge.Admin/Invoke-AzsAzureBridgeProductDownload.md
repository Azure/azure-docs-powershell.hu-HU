---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/22/2020
ms.locfileid: "93851122"
---
# <span data-ttu-id="53f89-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="53f89-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="53f89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53f89-102">SYNOPSIS</span></span>
<span data-ttu-id="53f89-103">A termékek letöltése az Azure Piactérről.</span><span class="sxs-lookup"><span data-stu-id="53f89-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="53f89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53f89-104">SYNTAX</span></span>

### <span data-ttu-id="53f89-105">Products_Download (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53f89-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53f89-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f89-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53f89-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="53f89-107">DESCRIPTION</span></span>
<span data-ttu-id="53f89-108">A termékek letöltése az Azure Piactérről.</span><span class="sxs-lookup"><span data-stu-id="53f89-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="53f89-109">Példák</span><span class="sxs-lookup"><span data-stu-id="53f89-109">EXAMPLES</span></span>

### <span data-ttu-id="53f89-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="53f89-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="53f89-111">Termékek letöltése az Azure Marketplace áruházból</span><span class="sxs-lookup"><span data-stu-id="53f89-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="53f89-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53f89-112">PARAMETERS</span></span>

### <span data-ttu-id="53f89-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53f89-113">-Name</span></span>
<span data-ttu-id="53f89-114">A szorzat neve</span><span class="sxs-lookup"><span data-stu-id="53f89-114">Name of the product</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f89-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="53f89-115">-ActivationName</span></span>
<span data-ttu-id="53f89-116">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="53f89-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f89-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f89-117">-ResourceGroupName</span></span>
<span data-ttu-id="53f89-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="53f89-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f89-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f89-119">-ResourceId</span></span>
<span data-ttu-id="53f89-120">Az Azure Bridge-termékek erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53f89-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="53f89-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53f89-121">-AsJob</span></span>
<span data-ttu-id="53f89-122">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="53f89-122">Run asynchronous as a job and return the job object.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f89-123">-Force</span><span class="sxs-lookup"><span data-stu-id="53f89-123">-Force</span></span>
<span data-ttu-id="53f89-124">A paraméter nem a megerősítés kérése</span><span class="sxs-lookup"><span data-stu-id="53f89-124">Switch parameter not to ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f89-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f89-125">-WhatIf</span></span>
<span data-ttu-id="53f89-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53f89-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f89-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53f89-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f89-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53f89-128">-Confirm</span></span>
<span data-ttu-id="53f89-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53f89-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f89-130">CommonParameters</span></span>
<span data-ttu-id="53f89-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53f89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f89-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f89-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f89-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53f89-133">INPUTS</span></span>

## <span data-ttu-id="53f89-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53f89-134">OUTPUTS</span></span>

## <span data-ttu-id="53f89-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53f89-135">NOTES</span></span>

## <span data-ttu-id="53f89-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53f89-136">RELATED LINKS</span></span>
