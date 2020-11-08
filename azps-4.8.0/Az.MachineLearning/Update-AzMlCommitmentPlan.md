---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181666"
---
# <span data-ttu-id="b5934-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b5934-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="b5934-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5934-102">SYNOPSIS</span></span>
<span data-ttu-id="b5934-103">Frissíti egy meglévő kötelezettségvállalási terv-erőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b5934-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="b5934-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5934-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5934-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5934-105">DESCRIPTION</span></span>
<span data-ttu-id="b5934-106">Frissíti a meglévő kötelezettségvállalási terv erőforrását.</span><span class="sxs-lookup"><span data-stu-id="b5934-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="b5934-107">Felhívjuk a figyelmét arra, hogy a kötelezettségvállalási terv legtöbb tulajdonsága megváltoztathatatlan, és nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="b5934-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="b5934-108">A módosítható tulajdonságok közé tartozik a SKU (amely lehetővé teszi a kötelezettségvállalási terv áttelepítését egy SKU-ról egy másikra) és a címkéket.</span><span class="sxs-lookup"><span data-stu-id="b5934-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="b5934-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b5934-109">EXAMPLES</span></span>

### <span data-ttu-id="b5934-110">Példa 1: kötelezettségvállalási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="b5934-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="b5934-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5934-111">PARAMETERS</span></span>

### <span data-ttu-id="b5934-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5934-112">-DefaultProfile</span></span>
<span data-ttu-id="b5934-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5934-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b5934-114">-Force</span></span>
<span data-ttu-id="b5934-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5934-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5934-116">-Name</span></span>
<span data-ttu-id="b5934-117">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="b5934-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5934-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5934-119">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b5934-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b5934-120">-SkuCapacity</span></span>
<span data-ttu-id="b5934-121">Az az SKU kapacitása, amelyet az Azure ML kötelezettségvállalási csomag frissítésekor kell használni.</span><span class="sxs-lookup"><span data-stu-id="b5934-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b5934-122">-SkuName</span></span>
<span data-ttu-id="b5934-123">Annak a SKU-nak a neve, amelyet az Azure ML kötelezettségvállalási csomag frissítésekor kell használni.</span><span class="sxs-lookup"><span data-stu-id="b5934-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b5934-124">-SkuTier</span></span>
<span data-ttu-id="b5934-125">Az az SKU-szint, amelyet az Azure ML kötelezettségvállalási csomag frissítésekor kell használni.</span><span class="sxs-lookup"><span data-stu-id="b5934-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="b5934-126">-Tag</span></span>
<span data-ttu-id="b5934-127">A kötelezettségvállalási terv erőforrásának címkéi</span><span class="sxs-lookup"><span data-stu-id="b5934-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5934-128">-Confirm</span></span>
<span data-ttu-id="b5934-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5934-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5934-130">-WhatIf</span></span>
<span data-ttu-id="b5934-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5934-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5934-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5934-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5934-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5934-133">CommonParameters</span></span>
<span data-ttu-id="b5934-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5934-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5934-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5934-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5934-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5934-136">INPUTS</span></span>

### <span data-ttu-id="b5934-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5934-137">None</span></span>

## <span data-ttu-id="b5934-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5934-138">OUTPUTS</span></span>

### <span data-ttu-id="b5934-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b5934-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="b5934-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5934-140">NOTES</span></span>
<span data-ttu-id="b5934-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="b5934-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b5934-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5934-142">RELATED LINKS</span></span>
