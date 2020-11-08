---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014231"
---
# <span data-ttu-id="dce0e-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dce0e-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="dce0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dce0e-102">SYNOPSIS</span></span>
<span data-ttu-id="dce0e-103">Egy kötelezettségvállalási terv törlése.</span><span class="sxs-lookup"><span data-stu-id="dce0e-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="dce0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dce0e-104">SYNTAX</span></span>

### <span data-ttu-id="dce0e-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dce0e-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce0e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="dce0e-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce0e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dce0e-107">DESCRIPTION</span></span>
<span data-ttu-id="dce0e-108">Az Azure Machine learning kötelezettségvállalási tervének törlése.</span><span class="sxs-lookup"><span data-stu-id="dce0e-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="dce0e-109">Felhívjuk a figyelmét arra, hogy a kötelezettségvállalási társításokat tartalmazó kötelezettségvállalási tervek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="dce0e-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="dce0e-110">A kötelezettségvállalási társításokat csak a cél-erőforrásokkal lehet törölni.</span><span class="sxs-lookup"><span data-stu-id="dce0e-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="dce0e-111">Ha például egy Azure Machine learning webszolgáltatást töröl, akkor az a kötelezettségvállalási társítás is törlődik, amely a webszolgáltatást társítja egy kötelezettségvállalási tervhez.</span><span class="sxs-lookup"><span data-stu-id="dce0e-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="dce0e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dce0e-112">EXAMPLES</span></span>

### <span data-ttu-id="dce0e-113">Példa 1: kötelezettségvállalási terv törlése</span><span class="sxs-lookup"><span data-stu-id="dce0e-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="dce0e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dce0e-114">PARAMETERS</span></span>

### <span data-ttu-id="dce0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce0e-115">-DefaultProfile</span></span>
<span data-ttu-id="dce0e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dce0e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dce0e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dce0e-117">-Force</span></span>
<span data-ttu-id="dce0e-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dce0e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dce0e-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dce0e-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="dce0e-120">A gépi tanulás webszolgáltatás objektuma.</span><span class="sxs-lookup"><span data-stu-id="dce0e-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="dce0e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dce0e-121">-Name</span></span>
<span data-ttu-id="dce0e-122">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="dce0e-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dce0e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce0e-123">-ResourceGroupName</span></span>
<span data-ttu-id="dce0e-124">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dce0e-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dce0e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dce0e-125">-Confirm</span></span>
<span data-ttu-id="dce0e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dce0e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce0e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce0e-127">-WhatIf</span></span>
<span data-ttu-id="dce0e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dce0e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dce0e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dce0e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce0e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce0e-130">CommonParameters</span></span>
<span data-ttu-id="dce0e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dce0e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce0e-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce0e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce0e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dce0e-133">INPUTS</span></span>

### <span data-ttu-id="dce0e-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dce0e-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="dce0e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dce0e-135">OUTPUTS</span></span>

### <span data-ttu-id="dce0e-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="dce0e-136">System.Void</span></span>

## <span data-ttu-id="dce0e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dce0e-137">NOTES</span></span>
<span data-ttu-id="dce0e-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="dce0e-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dce0e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dce0e-139">RELATED LINKS</span></span>
