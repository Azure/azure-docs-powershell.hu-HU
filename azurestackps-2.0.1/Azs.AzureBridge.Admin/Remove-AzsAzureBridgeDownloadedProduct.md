---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d75764209b56ed0cc05d80e00581de3f982e435
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/26/2020
ms.locfileid: "94017337"
---
# <span data-ttu-id="81773-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="81773-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="81773-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81773-102">SYNOPSIS</span></span>
<span data-ttu-id="81773-103">Az Azure piactérről letöltött termékek törlése</span><span class="sxs-lookup"><span data-stu-id="81773-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="81773-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81773-104">SYNTAX</span></span>

### <span data-ttu-id="81773-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81773-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81773-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="81773-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81773-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81773-107">DESCRIPTION</span></span>
<span data-ttu-id="81773-108">Az Azure piactérről letöltött termékek törlése</span><span class="sxs-lookup"><span data-stu-id="81773-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="81773-109">Példák</span><span class="sxs-lookup"><span data-stu-id="81773-109">EXAMPLES</span></span>

### <span data-ttu-id="81773-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="81773-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="81773-111">Az Azure piactérről letöltött termékek törlése</span><span class="sxs-lookup"><span data-stu-id="81773-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="81773-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81773-112">PARAMETERS</span></span>

### <span data-ttu-id="81773-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="81773-113">-ActivationName</span></span>
<span data-ttu-id="81773-114">Az aktiválás neve.</span><span class="sxs-lookup"><span data-stu-id="81773-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81773-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81773-115">-AsJob</span></span>
<span data-ttu-id="81773-116">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="81773-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="81773-117">-Force</span><span class="sxs-lookup"><span data-stu-id="81773-117">-Force</span></span>
<span data-ttu-id="81773-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81773-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="81773-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81773-119">-Name</span></span>
<span data-ttu-id="81773-120">A szorzat neve.</span><span class="sxs-lookup"><span data-stu-id="81773-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81773-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81773-121">-ResourceGroupName</span></span>
<span data-ttu-id="81773-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="81773-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81773-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81773-123">-ResourceId</span></span>
<span data-ttu-id="81773-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="81773-124">The resource id.</span></span>

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

### <span data-ttu-id="81773-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81773-125">-Confirm</span></span>
<span data-ttu-id="81773-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81773-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81773-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81773-127">-WhatIf</span></span>
<span data-ttu-id="81773-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81773-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81773-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81773-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81773-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81773-130">CommonParameters</span></span>
<span data-ttu-id="81773-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81773-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81773-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81773-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81773-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81773-133">INPUTS</span></span>

## <span data-ttu-id="81773-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81773-134">OUTPUTS</span></span>

### <span data-ttu-id="81773-135">Microsoft. AzureStack. Management. AzureBridge. admin. models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="81773-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="81773-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81773-136">NOTES</span></span>

## <span data-ttu-id="81773-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81773-137">RELATED LINKS</span></span>

