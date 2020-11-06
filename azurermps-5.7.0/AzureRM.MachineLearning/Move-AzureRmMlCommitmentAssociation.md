---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505496"
---
# <span data-ttu-id="0da51-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="0da51-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="0da51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0da51-102">SYNOPSIS</span></span>
<span data-ttu-id="0da51-103">A kötelezettségvállalási társítás áthelyezése az egyik kötelezettségvállalási tervből a másikba</span><span class="sxs-lookup"><span data-stu-id="0da51-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0da51-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0da51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0da51-105">DESCRIPTION</span></span>
<span data-ttu-id="0da51-106">Áthelyezi a kötelezettségvállalási társulás erőforrását a fölérendelt kötelezettségvállalási tervből egy másik kötelezettségvállalási csomagra.</span><span class="sxs-lookup"><span data-stu-id="0da51-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="0da51-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0da51-107">EXAMPLES</span></span>

### <span data-ttu-id="0da51-108">--------------------------Példa 1: kötelezettségvállalási társítás áthelyezése--------------------------</span><span class="sxs-lookup"><span data-stu-id="0da51-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="0da51-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0da51-109">PARAMETERS</span></span>

### <span data-ttu-id="0da51-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="0da51-110">-CommitmentPlanName</span></span>
<span data-ttu-id="0da51-111">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="0da51-111">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da51-112">-DefaultProfile</span></span>
<span data-ttu-id="0da51-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0da51-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da51-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="0da51-114">-DestinationPlanId</span></span>
<span data-ttu-id="0da51-115">Az Azure Resource ID a cél Azure ML kötelezettségvállalási csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="0da51-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da51-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0da51-116">-Name</span></span>
<span data-ttu-id="0da51-117">Az Azure ML kötelezettségvállalási társítás neve.</span><span class="sxs-lookup"><span data-stu-id="0da51-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da51-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da51-118">-ResourceGroupName</span></span>
<span data-ttu-id="0da51-119">Az Azure ML kötelezettségvállalási társítás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0da51-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da51-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0da51-120">-Confirm</span></span>
<span data-ttu-id="0da51-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0da51-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da51-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da51-122">-WhatIf</span></span>
<span data-ttu-id="0da51-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0da51-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0da51-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0da51-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da51-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da51-125">CommonParameters</span></span>
<span data-ttu-id="0da51-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0da51-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da51-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da51-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da51-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0da51-128">INPUTS</span></span>

### <span data-ttu-id="0da51-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="0da51-129">None</span></span>
<span data-ttu-id="0da51-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0da51-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0da51-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0da51-131">OUTPUTS</span></span>

### <span data-ttu-id="0da51-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0da51-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="0da51-133">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="0da51-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="0da51-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0da51-134">NOTES</span></span>
<span data-ttu-id="0da51-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="0da51-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0da51-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0da51-136">RELATED LINKS</span></span>

