---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194647"
---
# <span data-ttu-id="e302d-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="e302d-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="e302d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e302d-102">SYNOPSIS</span></span>
<span data-ttu-id="e302d-103">Lekérdezi egy vagy több kötelezettségvállalási társítás összefoglaló adatát.</span><span class="sxs-lookup"><span data-stu-id="e302d-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="e302d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e302d-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e302d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e302d-105">DESCRIPTION</span></span>
<span data-ttu-id="e302d-106">Kikeresi a kötelezettségvállalási társítás adatait.</span><span class="sxs-lookup"><span data-stu-id="e302d-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="e302d-107">Az átadott paraméterektől függően a parancsmag egy adott kötelezettségvállalási társítást vagy a meghatározott kötelezettségvállalási csomaghoz tartozó kötelezettségvállalási társításokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e302d-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="e302d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e302d-108">EXAMPLES</span></span>

### <span data-ttu-id="e302d-109">Példa 1: speciális kötelezettségvállalási társítás beszerzése</span><span class="sxs-lookup"><span data-stu-id="e302d-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="e302d-110">2. példa: a meghatározott kötelezettségvállalási csomag minden kötelezettségvállalási társításának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e302d-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="e302d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e302d-111">PARAMETERS</span></span>

### <span data-ttu-id="e302d-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="e302d-112">-CommitmentPlanName</span></span>
<span data-ttu-id="e302d-113">Annak az Azure ML-ös kötelezettségvállalási csomagnak a neve, amely egy vagy több kötelezettségvállalási társítással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e302d-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="e302d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e302d-114">-DefaultProfile</span></span>
<span data-ttu-id="e302d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e302d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e302d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e302d-116">-Name</span></span>
<span data-ttu-id="e302d-117">Az Azure ML kötelezettségvállalási társítás neve.</span><span class="sxs-lookup"><span data-stu-id="e302d-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e302d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e302d-118">-ResourceGroupName</span></span>
<span data-ttu-id="e302d-119">Az Azure ML kötelezettségvállalási társítás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e302d-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e302d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e302d-120">CommonParameters</span></span>
<span data-ttu-id="e302d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e302d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e302d-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e302d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e302d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e302d-123">INPUTS</span></span>

### <span data-ttu-id="e302d-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="e302d-124">None</span></span>

## <span data-ttu-id="e302d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e302d-125">OUTPUTS</span></span>

### <span data-ttu-id="e302d-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e302d-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="e302d-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e302d-127">NOTES</span></span>
<span data-ttu-id="e302d-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="e302d-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e302d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e302d-129">RELATED LINKS</span></span>