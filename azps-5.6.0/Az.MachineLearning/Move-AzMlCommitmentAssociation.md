---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: 019ff5b50eb366947f82004d60ae38888532ac10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918794"
---
# <span data-ttu-id="29d28-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="29d28-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="29d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d28-102">SYNOPSIS</span></span>
<span data-ttu-id="29d28-103">Kötelezettségvállalási társítást áthelyez egyik kötelezettségvállalási tervből a másikba.</span><span class="sxs-lookup"><span data-stu-id="29d28-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="29d28-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29d28-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29d28-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29d28-105">DESCRIPTION</span></span>
<span data-ttu-id="29d28-106">Áthelyez egy kötelezettségvállalási társítási erőforrást a szülő kötelezettségvállalási tervből egy másik kötelezettségvállalási csomagba.</span><span class="sxs-lookup"><span data-stu-id="29d28-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="29d28-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29d28-107">EXAMPLES</span></span>

### <span data-ttu-id="29d28-108">1. példa: Kötelezettségvállalási társítás áthelyezése</span><span class="sxs-lookup"><span data-stu-id="29d28-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="29d28-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29d28-109">PARAMETERS</span></span>

### <span data-ttu-id="29d28-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="29d28-110">-CommitmentPlanName</span></span>
<span data-ttu-id="29d28-111">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="29d28-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="29d28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d28-112">-DefaultProfile</span></span>
<span data-ttu-id="29d28-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29d28-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29d28-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="29d28-114">-DestinationPlanId</span></span>
<span data-ttu-id="29d28-115">A cél Azure ML-es kötelezettségvállalási csomagjának Azure-erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="29d28-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="29d28-116">-Name</span><span class="sxs-lookup"><span data-stu-id="29d28-116">-Name</span></span>
<span data-ttu-id="29d28-117">Az Azure ML kötelezettségvállalási társításának neve.</span><span class="sxs-lookup"><span data-stu-id="29d28-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="29d28-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d28-118">-ResourceGroupName</span></span>
<span data-ttu-id="29d28-119">Az Azure ML kötelezettségvállalási társításának erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="29d28-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="29d28-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29d28-120">-Confirm</span></span>
<span data-ttu-id="29d28-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="29d28-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29d28-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d28-122">-WhatIf</span></span>
<span data-ttu-id="29d28-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="29d28-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29d28-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29d28-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29d28-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d28-125">CommonParameters</span></span>
<span data-ttu-id="29d28-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d28-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d28-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d28-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d28-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29d28-128">INPUTS</span></span>

### <span data-ttu-id="29d28-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="29d28-129">None</span></span>

## <span data-ttu-id="29d28-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29d28-130">OUTPUTS</span></span>

### <span data-ttu-id="29d28-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="29d28-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="29d28-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29d28-132">NOTES</span></span>
<span data-ttu-id="29d28-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="29d28-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="29d28-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29d28-134">RELATED LINKS</span></span>
