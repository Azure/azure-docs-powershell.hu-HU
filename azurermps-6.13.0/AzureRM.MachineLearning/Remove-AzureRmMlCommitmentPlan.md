---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d14baa5382d5d9ffeeac8efd863a17cbad279865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502067"
---
# <span data-ttu-id="787e1-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="787e1-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="787e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="787e1-102">SYNOPSIS</span></span>
<span data-ttu-id="787e1-103">Egy kötelezettségvállalási terv törlése.</span><span class="sxs-lookup"><span data-stu-id="787e1-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="787e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="787e1-104">SYNTAX</span></span>

### <span data-ttu-id="787e1-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="787e1-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787e1-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="787e1-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="787e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="787e1-107">DESCRIPTION</span></span>
<span data-ttu-id="787e1-108">Az Azure Machine learning kötelezettségvállalási tervének törlése.</span><span class="sxs-lookup"><span data-stu-id="787e1-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="787e1-109">Felhívjuk a figyelmét arra, hogy a kötelezettségvállalási társításokat tartalmazó kötelezettségvállalási tervek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="787e1-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="787e1-110">A kötelezettségvállalási társításokat csak a cél-erőforrásokkal lehet törölni.</span><span class="sxs-lookup"><span data-stu-id="787e1-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="787e1-111">Ha például egy Azure Machine learning webszolgáltatást töröl, akkor az a kötelezettségvállalási társítás is törlődik, amely a webszolgáltatást társítja egy kötelezettségvállalási tervhez.</span><span class="sxs-lookup"><span data-stu-id="787e1-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="787e1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="787e1-112">EXAMPLES</span></span>

### <span data-ttu-id="787e1-113">Példa 1: kötelezettségvállalási terv törlése</span><span class="sxs-lookup"><span data-stu-id="787e1-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="787e1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="787e1-114">PARAMETERS</span></span>

### <span data-ttu-id="787e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787e1-115">-DefaultProfile</span></span>
<span data-ttu-id="787e1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="787e1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787e1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="787e1-117">-Force</span></span>
<span data-ttu-id="787e1-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="787e1-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="787e1-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="787e1-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="787e1-120">A gépi tanulás webszolgáltatás objektuma.</span><span class="sxs-lookup"><span data-stu-id="787e1-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="787e1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="787e1-121">-Name</span></span>
<span data-ttu-id="787e1-122">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="787e1-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="787e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="787e1-124">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="787e1-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="787e1-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="787e1-125">-Confirm</span></span>
<span data-ttu-id="787e1-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="787e1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787e1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="787e1-127">-WhatIf</span></span>
<span data-ttu-id="787e1-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="787e1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="787e1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="787e1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787e1-130">CommonParameters</span></span>
<span data-ttu-id="787e1-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="787e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787e1-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787e1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787e1-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="787e1-133">INPUTS</span></span>

### <span data-ttu-id="787e1-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="787e1-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="787e1-135">Paraméterek: MlCommitmentPlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="787e1-135">Parameters: MlCommitmentPlan (ByValue)</span></span>

## <span data-ttu-id="787e1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="787e1-136">OUTPUTS</span></span>

### <span data-ttu-id="787e1-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="787e1-137">System.Void</span></span>

## <span data-ttu-id="787e1-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="787e1-138">NOTES</span></span>
<span data-ttu-id="787e1-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="787e1-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="787e1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="787e1-140">RELATED LINKS</span></span>
