---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 5404cf82308c63a5ba6fe07ef4ac01101f44c48c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680154"
---
# <span data-ttu-id="0179a-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0179a-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="0179a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0179a-102">SYNOPSIS</span></span>
<span data-ttu-id="0179a-103">Lekérdezi egy vagy több kötelezettségvállalási terv összefoglaló adatát.</span><span class="sxs-lookup"><span data-stu-id="0179a-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0179a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0179a-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0179a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0179a-105">DESCRIPTION</span></span>
<span data-ttu-id="0179a-106">Kikeresi a kötelezettségvállalási terv adatait.</span><span class="sxs-lookup"><span data-stu-id="0179a-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="0179a-107">Az átadott paramenters függően a parancsmag egy konkrét kötelezettségvállalási tervet ad eredményül, amely egy adott erőforráscsoport számára az aktuális előfizetésben, illetve az aktuális előfizetéshez tartozó kötelezettségvállalási tervek gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="0179a-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="0179a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0179a-108">EXAMPLES</span></span>

### <span data-ttu-id="0179a-109">--------------------------Példa 1: speciális kötelezettségvállalási csomag beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="0179a-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="0179a-110">--------------------------Példa 2: a kötelezettségvállalási terv erőforrásainak beolvasása a jelenlegi előfizetésben--------------------------</span><span class="sxs-lookup"><span data-stu-id="0179a-110">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="0179a-111">--------------------------Példa 3: az összes kötelezettségvállalási terv beszerzése az aktuális előfizetésben és az adott erőforráscsoport--------------------------</span><span class="sxs-lookup"><span data-stu-id="0179a-111">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="0179a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0179a-112">PARAMETERS</span></span>

### <span data-ttu-id="0179a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0179a-113">-DefaultProfile</span></span>
<span data-ttu-id="0179a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0179a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0179a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0179a-115">-Name</span></span>
<span data-ttu-id="0179a-116">A kötelezettségvállalási terv neve.</span><span class="sxs-lookup"><span data-stu-id="0179a-116">The name of the commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0179a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0179a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0179a-118">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0179a-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0179a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0179a-119">CommonParameters</span></span>
<span data-ttu-id="0179a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0179a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0179a-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0179a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0179a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0179a-122">INPUTS</span></span>

### <span data-ttu-id="0179a-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="0179a-123">None</span></span>
<span data-ttu-id="0179a-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0179a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0179a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0179a-125">OUTPUTS</span></span>

### <span data-ttu-id="0179a-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0179a-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="0179a-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="0179a-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="0179a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0179a-128">NOTES</span></span>
<span data-ttu-id="0179a-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="0179a-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0179a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0179a-130">RELATED LINKS</span></span>

