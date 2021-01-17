---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346230"
---
# <span data-ttu-id="3f531-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3f531-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="3f531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f531-102">SYNOPSIS</span></span>
<span data-ttu-id="3f531-103">Egy kötelezettségvállalási terv törlése.</span><span class="sxs-lookup"><span data-stu-id="3f531-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="3f531-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f531-104">SYNTAX</span></span>

### <span data-ttu-id="3f531-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3f531-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f531-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3f531-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f531-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f531-107">DESCRIPTION</span></span>
<span data-ttu-id="3f531-108">Törli az Azure Machine Learning kötelezettségvállalási csomagját.</span><span class="sxs-lookup"><span data-stu-id="3f531-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="3f531-109">Felhívjuk a figyelmét arra, hogy a kötelezettségvállalási csomagokat nem lehet törölni.</span><span class="sxs-lookup"><span data-stu-id="3f531-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="3f531-110">A kötelezettségvállalási társításokat csak a célerőforrásuk tudja törölni.</span><span class="sxs-lookup"><span data-stu-id="3f531-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="3f531-111">Ha például töröl egy Azure Machine Learning webszolgáltatást, az azt a kötelezettségvállalási társítást is törli, amely a webszolgáltatást egy kötelezettségvállalási csomaghoz társítja.</span><span class="sxs-lookup"><span data-stu-id="3f531-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="3f531-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f531-112">EXAMPLES</span></span>

### <span data-ttu-id="3f531-113">1. példa: Kötelezettségvállalási terv törlése</span><span class="sxs-lookup"><span data-stu-id="3f531-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="3f531-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f531-114">PARAMETERS</span></span>

### <span data-ttu-id="3f531-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f531-115">-DefaultProfile</span></span>
<span data-ttu-id="3f531-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3f531-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f531-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3f531-117">-Force</span></span>
<span data-ttu-id="3f531-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f531-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3f531-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3f531-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="3f531-120">A gépi tanulási webszolgáltatás-objektum.</span><span class="sxs-lookup"><span data-stu-id="3f531-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f531-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3f531-121">-Name</span></span>
<span data-ttu-id="3f531-122">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="3f531-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f531-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f531-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f531-124">Az Azure ML kötelezettségvállalási terv erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="3f531-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f531-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f531-125">-Confirm</span></span>
<span data-ttu-id="3f531-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f531-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f531-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f531-127">-WhatIf</span></span>
<span data-ttu-id="3f531-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f531-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f531-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f531-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f531-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f531-130">CommonParameters</span></span>
<span data-ttu-id="3f531-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f531-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f531-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f531-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f531-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f531-133">INPUTS</span></span>

### <span data-ttu-id="3f531-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3f531-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3f531-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f531-135">OUTPUTS</span></span>

### <span data-ttu-id="3f531-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f531-136">System.Void</span></span>

## <span data-ttu-id="3f531-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f531-137">NOTES</span></span>
<span data-ttu-id="3f531-138">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="3f531-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3f531-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f531-139">RELATED LINKS</span></span>
