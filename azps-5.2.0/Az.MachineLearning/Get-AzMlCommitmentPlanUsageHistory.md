---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343577"
---
# <span data-ttu-id="636e9-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="636e9-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="636e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="636e9-102">SYNOPSIS</span></span>
<span data-ttu-id="636e9-103">Egy adott kötelezettségvállalási csomag használati előzményeinek adatait olvassa be.</span><span class="sxs-lookup"><span data-stu-id="636e9-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="636e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="636e9-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="636e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="636e9-105">DESCRIPTION</span></span>
<span data-ttu-id="636e9-106">Beolvassa egy adott kötelezettségvállalási terv használati előzményeinek adatait, beleértve a felhasznált erőforrásokat és a terven belül fennmaradó erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="636e9-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="636e9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="636e9-107">EXAMPLES</span></span>

### <span data-ttu-id="636e9-108">1. példa: Használati előzmények lekérte egy adott kötelezettségvállalási csomaghoz</span><span class="sxs-lookup"><span data-stu-id="636e9-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="636e9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="636e9-109">PARAMETERS</span></span>

### <span data-ttu-id="636e9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="636e9-110">-DefaultProfile</span></span>
<span data-ttu-id="636e9-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="636e9-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="636e9-112">-Name</span><span class="sxs-lookup"><span data-stu-id="636e9-112">-Name</span></span>
<span data-ttu-id="636e9-113">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="636e9-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="636e9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="636e9-114">-ResourceGroupName</span></span>
<span data-ttu-id="636e9-115">Az Azure ML kötelezettségvállalási terv erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="636e9-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="636e9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="636e9-116">CommonParameters</span></span>
<span data-ttu-id="636e9-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="636e9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="636e9-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="636e9-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="636e9-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="636e9-119">INPUTS</span></span>

### <span data-ttu-id="636e9-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="636e9-120">None</span></span>

## <span data-ttu-id="636e9-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="636e9-121">OUTPUTS</span></span>

### <span data-ttu-id="636e9-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="636e9-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="636e9-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="636e9-123">NOTES</span></span>
<span data-ttu-id="636e9-124">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="636e9-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="636e9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="636e9-125">RELATED LINKS</span></span>
