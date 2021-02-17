---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147571"
---
# <span data-ttu-id="17db0-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="17db0-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="17db0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17db0-102">SYNOPSIS</span></span>
<span data-ttu-id="17db0-103">Egy vagy több kötelezettségvállalási csomag összegző adatait olvassa be.</span><span class="sxs-lookup"><span data-stu-id="17db0-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="17db0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17db0-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17db0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17db0-105">DESCRIPTION</span></span>
<span data-ttu-id="17db0-106">Beolvassa a kötelezettségvállalási terv adatait.</span><span class="sxs-lookup"><span data-stu-id="17db0-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="17db0-107">A átadott paraméterektől függően a parancsmag adott kötelezettségvállalási tervet, az aktuális előfizetés egy adott erőforráscsoportra vonatkozó kötelezettségvállalási tervek gyűjteményét vagy a kötelezettségvállalási csomagok gyűjteményét adja vissza az aktuális előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="17db0-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="17db0-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17db0-108">EXAMPLES</span></span>

### <span data-ttu-id="17db0-109">1. példa: Konkrét kötelezettségvállalási csomag lekérte</span><span class="sxs-lookup"><span data-stu-id="17db0-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="17db0-110">2. példa: A kötelezettségvállalási terv összes erőforrásának lekérte az aktuális előfizetést</span><span class="sxs-lookup"><span data-stu-id="17db0-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="17db0-111">3. példa: Az aktuális előfizetés és adott erőforráscsoport összes kötelezettségvállalási csomagja</span><span class="sxs-lookup"><span data-stu-id="17db0-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="17db0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17db0-112">PARAMETERS</span></span>

### <span data-ttu-id="17db0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17db0-113">-DefaultProfile</span></span>
<span data-ttu-id="17db0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="17db0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17db0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="17db0-115">-Name</span></span>
<span data-ttu-id="17db0-116">A kötelezettségvállalási terv neve.</span><span class="sxs-lookup"><span data-stu-id="17db0-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="17db0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17db0-117">-ResourceGroupName</span></span>
<span data-ttu-id="17db0-118">Az Azure ML kötelezettségvállalási terv erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="17db0-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="17db0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17db0-119">CommonParameters</span></span>
<span data-ttu-id="17db0-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17db0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17db0-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17db0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17db0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17db0-122">INPUTS</span></span>

### <span data-ttu-id="17db0-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="17db0-123">None</span></span>

## <span data-ttu-id="17db0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17db0-124">OUTPUTS</span></span>

### <span data-ttu-id="17db0-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="17db0-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="17db0-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17db0-126">NOTES</span></span>
<span data-ttu-id="17db0-127">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="17db0-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="17db0-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17db0-128">RELATED LINKS</span></span>
