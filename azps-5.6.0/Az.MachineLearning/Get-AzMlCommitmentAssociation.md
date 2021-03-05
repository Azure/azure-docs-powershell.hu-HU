---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 9d58d8385d3f1d02e3bd823f43403d7dcdacf4a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012949"
---
# <span data-ttu-id="0bbc1-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="0bbc1-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="0bbc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bbc1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbc1-103">Egy vagy több kötelezettségvállalási társítás összegző adatait olvassa be.</span><span class="sxs-lookup"><span data-stu-id="0bbc1-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="0bbc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0bbc1-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bbc1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0bbc1-105">DESCRIPTION</span></span>
<span data-ttu-id="0bbc1-106">Beolvassa a kötelezettségvállalási társítás adatait.</span><span class="sxs-lookup"><span data-stu-id="0bbc1-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="0bbc1-107">A átadott paraméterektől függően a parancsmag adott kötelezettségvállalási társítást vagy kötelezettségvállalási társítások gyűjteményét adja vissza a megadott kötelezettségvállalási tervhez.</span><span class="sxs-lookup"><span data-stu-id="0bbc1-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="0bbc1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0bbc1-108">EXAMPLES</span></span>

### <span data-ttu-id="0bbc1-109">1. példa: Konkrét kötelezettségvállalási társítás lekérte</span><span class="sxs-lookup"><span data-stu-id="0bbc1-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="0bbc1-110">2. példa: A megadott kötelezettségvállalási csomag összes kötelezettségvállalási társításának lekérte</span><span class="sxs-lookup"><span data-stu-id="0bbc1-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="0bbc1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bbc1-111">PARAMETERS</span></span>

### <span data-ttu-id="0bbc1-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="0bbc1-112">-CommitmentPlanName</span></span>
<span data-ttu-id="0bbc1-113">Annak az Azure ML-beli kötelezettségvállalási csomagnak a neve, amely egy vagy több kötelezettségvállalási társítást tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0bbc1-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="0bbc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbc1-114">-DefaultProfile</span></span>
<span data-ttu-id="0bbc1-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0bbc1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bbc1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0bbc1-116">-Name</span></span>
<span data-ttu-id="0bbc1-117">Az Azure ML kötelezettségvállalási társításának neve.</span><span class="sxs-lookup"><span data-stu-id="0bbc1-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="0bbc1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbc1-118">-ResourceGroupName</span></span>
<span data-ttu-id="0bbc1-119">Az Azure ML kötelezettségvállalási társításának erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="0bbc1-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="0bbc1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbc1-120">CommonParameters</span></span>
<span data-ttu-id="0bbc1-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bbc1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbc1-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bbc1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbc1-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bbc1-123">INPUTS</span></span>

### <span data-ttu-id="0bbc1-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="0bbc1-124">None</span></span>

## <span data-ttu-id="0bbc1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bbc1-125">OUTPUTS</span></span>

### <span data-ttu-id="0bbc1-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0bbc1-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="0bbc1-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0bbc1-127">NOTES</span></span>
<span data-ttu-id="0bbc1-128">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="0bbc1-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0bbc1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bbc1-129">RELATED LINKS</span></span>
