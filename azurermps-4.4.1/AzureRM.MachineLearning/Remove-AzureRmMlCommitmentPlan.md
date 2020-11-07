---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 31678552a43951406d18c49ee80ffaa7897fd1d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680869"
---
# <span data-ttu-id="2ea62-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2ea62-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="2ea62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ea62-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea62-103">Egy kötelezettségvállalási terv törlése.</span><span class="sxs-lookup"><span data-stu-id="2ea62-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ea62-104">SYNTAX</span></span>

### <span data-ttu-id="2ea62-105">A név és az erőforráscsoport mezőben megadott Azure ML-es kötelezettségvállalási csomag eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2ea62-105">Remove an Azure ML commitment plan specified by name and resource group.</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea62-106">Objektumként megadott Azure ML-es kötelezettségvállalási terv eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2ea62-106">Remove an Azure ML commitment plan specified as an object.</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea62-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ea62-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea62-108">Az Azure Machine learning kötelezettségvállalási tervének törlése.</span><span class="sxs-lookup"><span data-stu-id="2ea62-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="2ea62-109">Felhívjuk a figyelmét arra, hogy a kötelezettségvállalási társításokat tartalmazó kötelezettségvállalási tervek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="2ea62-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="2ea62-110">A kötelezettségvállalási társításokat csak a cél-erőforrásokkal lehet törölni.</span><span class="sxs-lookup"><span data-stu-id="2ea62-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="2ea62-111">Ha például egy Azure Machine learning webszolgáltatást töröl, akkor az a kötelezettségvállalási társítás is törlődik, amely a webszolgáltatást társítja egy kötelezettségvállalási tervhez.</span><span class="sxs-lookup"><span data-stu-id="2ea62-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="2ea62-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2ea62-112">EXAMPLES</span></span>

### <span data-ttu-id="2ea62-113">--------------------------Példa 1: kötelezettségvállalási terv törlése--------------------------</span><span class="sxs-lookup"><span data-stu-id="2ea62-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
<span data-ttu-id="2ea62-114">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="2ea62-114">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="2ea62-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ea62-115">PARAMETERS</span></span>

### <span data-ttu-id="2ea62-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2ea62-116">-Force</span></span>
<span data-ttu-id="2ea62-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ea62-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2ea62-118">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2ea62-118">-MlCommitmentPlan</span></span>
<span data-ttu-id="2ea62-119">A gépi tanulás webszolgáltatás objektuma.</span><span class="sxs-lookup"><span data-stu-id="2ea62-119">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: Remove an Azure ML commitment plan specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ea62-120">-Name</span></span>
<span data-ttu-id="2ea62-121">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="2ea62-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea62-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ea62-123">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ea62-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea62-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ea62-124">-Confirm</span></span>
<span data-ttu-id="2ea62-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ea62-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea62-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea62-126">-WhatIf</span></span>
<span data-ttu-id="2ea62-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ea62-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ea62-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ea62-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea62-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea62-129">-DefaultProfile</span></span>
<span data-ttu-id="2ea62-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ea62-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea62-131">CommonParameters</span></span>
<span data-ttu-id="2ea62-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ea62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea62-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea62-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea62-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ea62-134">INPUTS</span></span>

### <span data-ttu-id="2ea62-135">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2ea62-135">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="2ea62-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ea62-136">OUTPUTS</span></span>

### <span data-ttu-id="2ea62-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ea62-137">None</span></span>

## <span data-ttu-id="2ea62-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ea62-138">NOTES</span></span>
<span data-ttu-id="2ea62-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="2ea62-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2ea62-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ea62-140">RELATED LINKS</span></span>

