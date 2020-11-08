---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181671"
---
# <span data-ttu-id="3d088-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3d088-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="3d088-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d088-102">SYNOPSIS</span></span>
<span data-ttu-id="3d088-103">Lekérdezi egy vagy több kötelezettségvállalási terv összefoglaló adatát.</span><span class="sxs-lookup"><span data-stu-id="3d088-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="3d088-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d088-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d088-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d088-105">DESCRIPTION</span></span>
<span data-ttu-id="3d088-106">Kikeresi a kötelezettségvállalási terv adatait.</span><span class="sxs-lookup"><span data-stu-id="3d088-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="3d088-107">Az átadott paraméterektől függően a parancsmag egy konkrét kötelezettségvállalási csomagot ad eredményül, amely egy adott erőforráscsoport számára az aktuális előfizetésben megadott erőforráscsoport, illetve az aktuális előfizetéshez tartozó kötelezettségvállalási tervek gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="3d088-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="3d088-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3d088-108">EXAMPLES</span></span>

### <span data-ttu-id="3d088-109">Példa 1: konkrét kötelezettségvállalási terv beszerzése</span><span class="sxs-lookup"><span data-stu-id="3d088-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="3d088-110">2. példa: az összes kötelezettségvállalási terv erőforrásainak beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="3d088-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="3d088-111">3. példa: az összes kötelezettségvállalási terv beszerzése az aktuális előfizetésben és az adott erőforráscsoportben</span><span class="sxs-lookup"><span data-stu-id="3d088-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="3d088-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d088-112">PARAMETERS</span></span>

### <span data-ttu-id="3d088-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d088-113">-DefaultProfile</span></span>
<span data-ttu-id="3d088-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3d088-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d088-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d088-115">-Name</span></span>
<span data-ttu-id="3d088-116">A kötelezettségvállalási terv neve.</span><span class="sxs-lookup"><span data-stu-id="3d088-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="3d088-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d088-117">-ResourceGroupName</span></span>
<span data-ttu-id="3d088-118">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3d088-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d088-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d088-119">CommonParameters</span></span>
<span data-ttu-id="3d088-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d088-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d088-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d088-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d088-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d088-122">INPUTS</span></span>

### <span data-ttu-id="3d088-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d088-123">None</span></span>

## <span data-ttu-id="3d088-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d088-124">OUTPUTS</span></span>

### <span data-ttu-id="3d088-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3d088-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3d088-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d088-126">NOTES</span></span>
<span data-ttu-id="3d088-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="3d088-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3d088-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d088-128">RELATED LINKS</span></span>
