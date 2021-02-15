---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207271"
---
# <span data-ttu-id="6b20f-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6b20f-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="6b20f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b20f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b20f-103">Létrehoz egy új kötelezettségvállalási tervet.</span><span class="sxs-lookup"><span data-stu-id="6b20f-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="6b20f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b20f-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b20f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b20f-105">DESCRIPTION</span></span>
<span data-ttu-id="6b20f-106">Azure Machine Learning-alapú kötelezettségvállalási tervet hoz létre egy meglévő erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6b20f-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="6b20f-107">Ha az erőforráscsoportban létezik azonos nevű kötelezettségvállalási terv, a hívás frissítési műveletként működik, és a meglévő kötelezettségvállalási terv felülíródik.</span><span class="sxs-lookup"><span data-stu-id="6b20f-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="6b20f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b20f-108">EXAMPLES</span></span>

### <span data-ttu-id="6b20f-109">1. példa: Új kötelezettségvállalási terv létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b20f-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="6b20f-110">Létrehozza a MyCommitmentPlanName nevű új Azure Machine Learning-beli kötelezettségvállalási tervet a "MyResourceGroup" csoportban és az Egyesült Államok déli részén.</span><span class="sxs-lookup"><span data-stu-id="6b20f-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="6b20f-111">Ebben a példában az SKU DevTest/Standard függvényt használjuk, ami azt jelenti, hogy a kötelezettségvállalási terv által biztosított erőforrásokat a DevTest/Standard korlátai határozzák meg.</span><span class="sxs-lookup"><span data-stu-id="6b20f-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="6b20f-112">Ebben a példában a SkuCapacity érték 1, ami azt jelenti, hogy a terv költsége a DevTest költségének 1-edike lesz, és a tervben található erőforrások a DevTest által rendelkezésre álló 1-edik erőforrást fogják tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="6b20f-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="6b20f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b20f-113">PARAMETERS</span></span>

### <span data-ttu-id="6b20f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b20f-114">-DefaultProfile</span></span>
<span data-ttu-id="6b20f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6b20f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b20f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6b20f-116">-Force</span></span>
<span data-ttu-id="6b20f-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b20f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6b20f-118">-Location</span><span class="sxs-lookup"><span data-stu-id="6b20f-118">-Location</span></span>
<span data-ttu-id="6b20f-119">Az Azure ML kötelezettségvállalási csomagja.</span><span class="sxs-lookup"><span data-stu-id="6b20f-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b20f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6b20f-120">-Name</span></span>
<span data-ttu-id="6b20f-121">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="6b20f-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b20f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b20f-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b20f-123">Az Azure ML kötelezettségvállalási terv erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="6b20f-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b20f-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6b20f-124">-SkuCapacity</span></span>
<span data-ttu-id="6b20f-125">Az Azure ML kötelezettségvállalási csomag kiépítésekor használható termékváltozat kapacitása.</span><span class="sxs-lookup"><span data-stu-id="6b20f-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b20f-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6b20f-126">-SkuName</span></span>
<span data-ttu-id="6b20f-127">Az Azure ML kötelezettségvállalási csomag kiépítésekor használt termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="6b20f-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b20f-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6b20f-128">-SkuTier</span></span>
<span data-ttu-id="6b20f-129">Az Azure ML-es kötelezettségvállalási csomag kiépítésekor használt termékváltozat rétege.</span><span class="sxs-lookup"><span data-stu-id="6b20f-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b20f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b20f-130">-Confirm</span></span>
<span data-ttu-id="6b20f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b20f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b20f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b20f-132">-WhatIf</span></span>
<span data-ttu-id="6b20f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b20f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b20f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b20f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b20f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b20f-135">CommonParameters</span></span>
<span data-ttu-id="6b20f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b20f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b20f-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b20f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b20f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b20f-138">INPUTS</span></span>

### <span data-ttu-id="6b20f-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b20f-139">None</span></span>

## <span data-ttu-id="6b20f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b20f-140">OUTPUTS</span></span>

### <span data-ttu-id="6b20f-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6b20f-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="6b20f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b20f-142">NOTES</span></span>
<span data-ttu-id="6b20f-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="6b20f-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6b20f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b20f-144">RELATED LINKS</span></span>
