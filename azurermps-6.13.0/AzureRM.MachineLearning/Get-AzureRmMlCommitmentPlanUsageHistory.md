---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 481d1e26ad769101f06acda5573175bd06331fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505376"
---
# <span data-ttu-id="552c2-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="552c2-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="552c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="552c2-102">SYNOPSIS</span></span>
<span data-ttu-id="552c2-103">A megadott kötelezettségvállalási csomag használati előzményeit olvassa fel.</span><span class="sxs-lookup"><span data-stu-id="552c2-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="552c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="552c2-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="552c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="552c2-105">DESCRIPTION</span></span>
<span data-ttu-id="552c2-106">Beolvassa a használati előzmények adatait egy meghatározott kötelezettségvállalási tervhez, benne a felhasznált erőforrásokkal és a tervben fennmaradó erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="552c2-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="552c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="552c2-107">EXAMPLES</span></span>

### <span data-ttu-id="552c2-108">Példa 1: meghatározott kötelezettségvállalási terv használati előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="552c2-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="552c2-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="552c2-109">PARAMETERS</span></span>

### <span data-ttu-id="552c2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="552c2-110">-DefaultProfile</span></span>
<span data-ttu-id="552c2-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="552c2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="552c2-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="552c2-112">-Name</span></span>
<span data-ttu-id="552c2-113">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="552c2-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="552c2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="552c2-114">-ResourceGroupName</span></span>
<span data-ttu-id="552c2-115">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="552c2-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="552c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="552c2-116">CommonParameters</span></span>
<span data-ttu-id="552c2-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="552c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="552c2-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="552c2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="552c2-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="552c2-119">INPUTS</span></span>

### <span data-ttu-id="552c2-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="552c2-120">None</span></span>

## <span data-ttu-id="552c2-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="552c2-121">OUTPUTS</span></span>

### <span data-ttu-id="552c2-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="552c2-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="552c2-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="552c2-123">NOTES</span></span>
<span data-ttu-id="552c2-124">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="552c2-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="552c2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="552c2-125">RELATED LINKS</span></span>
