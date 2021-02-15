---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159499"
---
# <span data-ttu-id="2b9ee-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2b9ee-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="2b9ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9ee-103">Frissíti egy meglévő kötelezettségvállalási terv típusú erőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="2b9ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b9ee-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b9ee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b9ee-105">DESCRIPTION</span></span>
<span data-ttu-id="2b9ee-106">Frissíti a meglévő kötelezettségvállalási terv erőforrását.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="2b9ee-107">Ne feledje, hogy a kötelezettségvállalási terv legtöbb tulajdonsága nem módosítható, és nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="2b9ee-108">A módosítható tulajdonságok közé tartozik a termékváltozat (lehetővé teszi a kötelezettségvállalási terv áttelepítését egyik termékváltozatból a másikba) és a címkéket.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="2b9ee-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b9ee-109">EXAMPLES</span></span>

### <span data-ttu-id="2b9ee-110">1. példa: Kötelezettségvállalási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="2b9ee-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="2b9ee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b9ee-111">PARAMETERS</span></span>

### <span data-ttu-id="2b9ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9ee-112">-DefaultProfile</span></span>
<span data-ttu-id="2b9ee-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b9ee-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b9ee-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2b9ee-114">-Force</span></span>
<span data-ttu-id="2b9ee-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2b9ee-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2b9ee-116">-Name</span></span>
<span data-ttu-id="2b9ee-117">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b9ee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9ee-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b9ee-119">Az Azure ML kötelezettségvállalási terv erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b9ee-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2b9ee-120">-SkuCapacity</span></span>
<span data-ttu-id="2b9ee-121">Az Azure ML kötelezettségvállalási csomag frissítésekhez használható termékváltozatának kapacitása.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b9ee-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b9ee-122">-SkuName</span></span>
<span data-ttu-id="2b9ee-123">Az Azure ML kötelezettségvállalási csomag frissítésekéhez használt termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b9ee-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2b9ee-124">-SkuTier</span></span>
<span data-ttu-id="2b9ee-125">Az Azure ML kötelezettségvállalási csomag frissítésekhez használt termékváltozatának rétege.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b9ee-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b9ee-126">-Tag</span></span>
<span data-ttu-id="2b9ee-127">A kötelezettségvállalási terv erőforrásának címkéi.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="2b9ee-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b9ee-128">-Confirm</span></span>
<span data-ttu-id="2b9ee-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9ee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9ee-130">-WhatIf</span></span>
<span data-ttu-id="2b9ee-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b9ee-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9ee-133">CommonParameters</span></span>
<span data-ttu-id="2b9ee-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9ee-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b9ee-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9ee-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b9ee-136">INPUTS</span></span>

### <span data-ttu-id="2b9ee-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b9ee-137">None</span></span>

## <span data-ttu-id="2b9ee-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b9ee-138">OUTPUTS</span></span>

### <span data-ttu-id="2b9ee-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2b9ee-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="2b9ee-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b9ee-140">NOTES</span></span>
<span data-ttu-id="2b9ee-141">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="2b9ee-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2b9ee-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b9ee-142">RELATED LINKS</span></span>
