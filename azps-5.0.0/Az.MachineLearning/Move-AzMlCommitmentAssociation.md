---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194640"
---
# <span data-ttu-id="03eb0-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="03eb0-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="03eb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="03eb0-103">A kötelezettségvállalási társítás áthelyezése az egyik kötelezettségvállalási tervből a másikba</span><span class="sxs-lookup"><span data-stu-id="03eb0-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="03eb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03eb0-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03eb0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="03eb0-106">Áthelyezi a kötelezettségvállalási társulás erőforrását a fölérendelt kötelezettségvállalási tervből egy másik kötelezettségvállalási csomagra.</span><span class="sxs-lookup"><span data-stu-id="03eb0-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="03eb0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03eb0-107">EXAMPLES</span></span>

### <span data-ttu-id="03eb0-108">1. példa: kötelezettségvállalási társítás áthelyezése</span><span class="sxs-lookup"><span data-stu-id="03eb0-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="03eb0-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03eb0-109">PARAMETERS</span></span>

### <span data-ttu-id="03eb0-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="03eb0-110">-CommitmentPlanName</span></span>
<span data-ttu-id="03eb0-111">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="03eb0-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="03eb0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03eb0-112">-DefaultProfile</span></span>
<span data-ttu-id="03eb0-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="03eb0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03eb0-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="03eb0-114">-DestinationPlanId</span></span>
<span data-ttu-id="03eb0-115">Az Azure Resource ID a cél Azure ML kötelezettségvállalási csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="03eb0-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="03eb0-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03eb0-116">-Name</span></span>
<span data-ttu-id="03eb0-117">Az Azure ML kötelezettségvállalási társítás neve.</span><span class="sxs-lookup"><span data-stu-id="03eb0-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="03eb0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03eb0-118">-ResourceGroupName</span></span>
<span data-ttu-id="03eb0-119">Az Azure ML kötelezettségvállalási társítás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03eb0-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="03eb0-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03eb0-120">-Confirm</span></span>
<span data-ttu-id="03eb0-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03eb0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03eb0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03eb0-122">-WhatIf</span></span>
<span data-ttu-id="03eb0-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03eb0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03eb0-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03eb0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03eb0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03eb0-125">CommonParameters</span></span>
<span data-ttu-id="03eb0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03eb0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03eb0-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03eb0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03eb0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03eb0-128">INPUTS</span></span>

### <span data-ttu-id="03eb0-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="03eb0-129">None</span></span>

## <span data-ttu-id="03eb0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03eb0-130">OUTPUTS</span></span>

### <span data-ttu-id="03eb0-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="03eb0-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="03eb0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03eb0-132">NOTES</span></span>
<span data-ttu-id="03eb0-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="03eb0-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="03eb0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03eb0-134">RELATED LINKS</span></span>
