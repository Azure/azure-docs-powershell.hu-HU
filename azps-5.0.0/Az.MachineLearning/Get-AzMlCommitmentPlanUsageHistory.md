---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195822"
---
# <span data-ttu-id="ed0a7-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="ed0a7-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="ed0a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0a7-103">A megadott kötelezettségvállalási csomag használati előzményeit olvassa fel.</span><span class="sxs-lookup"><span data-stu-id="ed0a7-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="ed0a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed0a7-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed0a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0a7-106">Beolvassa a használati előzmények adatait egy meghatározott kötelezettségvállalási tervhez, benne a felhasznált erőforrásokkal és a tervben fennmaradó erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="ed0a7-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="ed0a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ed0a7-107">EXAMPLES</span></span>

### <span data-ttu-id="ed0a7-108">Példa 1: meghatározott kötelezettségvállalási terv használati előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed0a7-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="ed0a7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed0a7-109">PARAMETERS</span></span>

### <span data-ttu-id="ed0a7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0a7-110">-DefaultProfile</span></span>
<span data-ttu-id="ed0a7-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ed0a7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed0a7-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed0a7-112">-Name</span></span>
<span data-ttu-id="ed0a7-113">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="ed0a7-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ed0a7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed0a7-114">-ResourceGroupName</span></span>
<span data-ttu-id="ed0a7-115">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed0a7-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ed0a7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0a7-116">CommonParameters</span></span>
<span data-ttu-id="ed0a7-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed0a7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0a7-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0a7-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0a7-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed0a7-119">INPUTS</span></span>

### <span data-ttu-id="ed0a7-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="ed0a7-120">None</span></span>

## <span data-ttu-id="ed0a7-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed0a7-121">OUTPUTS</span></span>

### <span data-ttu-id="ed0a7-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="ed0a7-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="ed0a7-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed0a7-123">NOTES</span></span>
<span data-ttu-id="ed0a7-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="ed0a7-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ed0a7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed0a7-125">RELATED LINKS</span></span>