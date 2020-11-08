---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7ca58f806f4d63f2938e3934838a40cbbb113b2
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/26/2020
ms.locfileid: "94017338"
---
# <span data-ttu-id="0f764-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="0f764-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="0f764-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f764-102">SYNOPSIS</span></span>
<span data-ttu-id="0f764-103">A termékek letöltése az Azure Piactérről.</span><span class="sxs-lookup"><span data-stu-id="0f764-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="0f764-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f764-104">SYNTAX</span></span>

### <span data-ttu-id="0f764-105">Products_Download (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f764-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f764-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f764-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f764-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f764-107">DESCRIPTION</span></span>
<span data-ttu-id="0f764-108">A termékek letöltése az Azure Piactérről.</span><span class="sxs-lookup"><span data-stu-id="0f764-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="0f764-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0f764-109">EXAMPLES</span></span>

### <span data-ttu-id="0f764-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f764-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="0f764-111">Termékek letöltése az Azure Marketplace áruházból</span><span class="sxs-lookup"><span data-stu-id="0f764-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="0f764-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f764-112">PARAMETERS</span></span>

### <span data-ttu-id="0f764-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="0f764-113">-ActivationName</span></span>
<span data-ttu-id="0f764-114">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="0f764-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f764-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f764-115">-AsJob</span></span>
<span data-ttu-id="0f764-116">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="0f764-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0f764-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0f764-117">-Force</span></span>
<span data-ttu-id="0f764-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f764-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0f764-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f764-119">-Name</span></span>
<span data-ttu-id="0f764-120">A szorzat neve.</span><span class="sxs-lookup"><span data-stu-id="0f764-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f764-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f764-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f764-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="0f764-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f764-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f764-123">-ResourceId</span></span>
<span data-ttu-id="0f764-124">Az Azure Bridge-termékek erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0f764-124">Resource identifier for azure bridge product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f764-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f764-125">-Confirm</span></span>
<span data-ttu-id="0f764-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f764-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f764-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f764-127">-WhatIf</span></span>
<span data-ttu-id="0f764-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f764-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f764-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f764-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f764-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f764-130">CommonParameters</span></span>
<span data-ttu-id="0f764-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f764-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f764-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f764-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f764-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f764-133">INPUTS</span></span>

## <span data-ttu-id="0f764-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f764-134">OUTPUTS</span></span>

## <span data-ttu-id="0f764-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f764-135">NOTES</span></span>

## <span data-ttu-id="0f764-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f764-136">RELATED LINKS</span></span>

