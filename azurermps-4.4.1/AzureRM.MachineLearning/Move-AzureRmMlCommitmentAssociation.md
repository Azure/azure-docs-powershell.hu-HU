---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504892"
---
# <span data-ttu-id="97e20-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="97e20-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="97e20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97e20-102">SYNOPSIS</span></span>
<span data-ttu-id="97e20-103">A kötelezettségvállalási társítás áthelyezése az egyik kötelezettségvállalási tervből a másikba</span><span class="sxs-lookup"><span data-stu-id="97e20-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97e20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97e20-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97e20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97e20-105">DESCRIPTION</span></span>
<span data-ttu-id="97e20-106">Áthelyezi a kötelezettségvállalási társulás erőforrását a fölérendelt kötelezettségvállalási tervből egy másik kötelezettségvállalási csomagra.</span><span class="sxs-lookup"><span data-stu-id="97e20-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="97e20-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97e20-107">EXAMPLES</span></span>

### <span data-ttu-id="97e20-108">--------------------------Példa 1: kötelezettségvállalási társítás áthelyezése--------------------------</span><span class="sxs-lookup"><span data-stu-id="97e20-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="97e20-109">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="97e20-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="97e20-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97e20-110">PARAMETERS</span></span>

### <span data-ttu-id="97e20-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="97e20-111">-CommitmentPlanName</span></span>
<span data-ttu-id="97e20-112">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="97e20-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97e20-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="97e20-113">-DestinationPlanId</span></span>
<span data-ttu-id="97e20-114">Az Azure Resource ID a cél Azure ML kötelezettségvállalási csomaghoz.</span><span class="sxs-lookup"><span data-stu-id="97e20-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97e20-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97e20-115">-Name</span></span>
<span data-ttu-id="97e20-116">Az Azure ML kötelezettségvállalási társítás neve.</span><span class="sxs-lookup"><span data-stu-id="97e20-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="97e20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e20-117">-ResourceGroupName</span></span>
<span data-ttu-id="97e20-118">Az Azure ML kötelezettségvállalási társítás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="97e20-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="97e20-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97e20-119">-Confirm</span></span>
<span data-ttu-id="97e20-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97e20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e20-121">-WhatIf</span></span>
<span data-ttu-id="97e20-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97e20-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97e20-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97e20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e20-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e20-124">-DefaultProfile</span></span>
<span data-ttu-id="97e20-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97e20-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97e20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e20-126">CommonParameters</span></span>
<span data-ttu-id="97e20-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97e20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e20-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e20-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e20-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e20-129">INPUTS</span></span>

## <span data-ttu-id="97e20-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e20-130">OUTPUTS</span></span>

### <span data-ttu-id="97e20-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="97e20-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="97e20-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="97e20-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="97e20-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97e20-133">NOTES</span></span>
<span data-ttu-id="97e20-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="97e20-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="97e20-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97e20-135">RELATED LINKS</span></span>

