---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93680919"
---
# <span data-ttu-id="8ba5c-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="8ba5c-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="8ba5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ba5c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba5c-103">A megadott kötelezettségvállalási csomag használati előzményeit olvassa fel.</span><span class="sxs-lookup"><span data-stu-id="8ba5c-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ba5c-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ba5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ba5c-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba5c-106">Beolvassa a használati előzmények adatait egy meghatározott kötelezettségvállalási tervhez, benne a felhasznált erőforrásokkal és a tervben fennmaradó erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="8ba5c-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="8ba5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8ba5c-107">EXAMPLES</span></span>

### <span data-ttu-id="8ba5c-108">--------------------------Példa 1: meghatározott kötelezettségvállalási terv használati előzményeinek beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ba5c-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="8ba5c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ba5c-109">PARAMETERS</span></span>

### <span data-ttu-id="8ba5c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba5c-110">-DefaultProfile</span></span>
<span data-ttu-id="8ba5c-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8ba5c-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba5c-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ba5c-112">-Name</span></span>
<span data-ttu-id="8ba5c-113">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="8ba5c-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba5c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba5c-114">-ResourceGroupName</span></span>
<span data-ttu-id="8ba5c-115">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ba5c-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba5c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba5c-116">CommonParameters</span></span>
<span data-ttu-id="8ba5c-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ba5c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba5c-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba5c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba5c-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba5c-119">INPUTS</span></span>

### <span data-ttu-id="8ba5c-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="8ba5c-120">None</span></span>
<span data-ttu-id="8ba5c-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8ba5c-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ba5c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ba5c-122">OUTPUTS</span></span>

### <span data-ttu-id="8ba5c-123">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="8ba5c-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="8ba5c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ba5c-124">NOTES</span></span>
<span data-ttu-id="8ba5c-125">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="8ba5c-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8ba5c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ba5c-126">RELATED LINKS</span></span>

