---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 3be16cd371543848d650711241dbcb8828a5ba32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503739"
---
# <span data-ttu-id="72c02-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="72c02-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="72c02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72c02-102">SYNOPSIS</span></span>
<span data-ttu-id="72c02-103">Lekérdezi egy vagy több kötelezettségvállalási társítás összefoglaló adatát.</span><span class="sxs-lookup"><span data-stu-id="72c02-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72c02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72c02-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72c02-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72c02-105">DESCRIPTION</span></span>
<span data-ttu-id="72c02-106">Kikeresi a kötelezettségvállalási társítás adatait.</span><span class="sxs-lookup"><span data-stu-id="72c02-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="72c02-107">Az átadott paramenters függően a parancsmag egy adott kötelezettségvállalási társítást vagy a meghatározott kötelezettségvállalási csomaghoz tartozó kötelezettségvállalási társításokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="72c02-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="72c02-108">Példák</span><span class="sxs-lookup"><span data-stu-id="72c02-108">EXAMPLES</span></span>

### <span data-ttu-id="72c02-109">--------------------------Példa 1: speciális kötelezettségvállalási társítás beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="72c02-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="72c02-110">--------------------------Példa 2: a meghatározott kötelezettségvállalási csomaghoz tartozó összes kötelezettségvállalási társítás beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="72c02-110">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="72c02-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72c02-111">PARAMETERS</span></span>

### <span data-ttu-id="72c02-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="72c02-112">-CommitmentPlanName</span></span>
<span data-ttu-id="72c02-113">Annak az Azure ML-ös kötelezettségvállalási csomagnak a neve, amely egy vagy több kötelezettségvállalási társítással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="72c02-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="72c02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c02-114">-DefaultProfile</span></span>
<span data-ttu-id="72c02-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="72c02-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72c02-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72c02-116">-Name</span></span>
<span data-ttu-id="72c02-117">Az Azure ML kötelezettségvállalási társítás neve.</span><span class="sxs-lookup"><span data-stu-id="72c02-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="72c02-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c02-118">-ResourceGroupName</span></span>
<span data-ttu-id="72c02-119">Az Azure ML kötelezettségvállalási társítás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="72c02-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="72c02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c02-120">CommonParameters</span></span>
<span data-ttu-id="72c02-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72c02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c02-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c02-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c02-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72c02-123">INPUTS</span></span>

### <span data-ttu-id="72c02-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="72c02-124">None</span></span>
<span data-ttu-id="72c02-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="72c02-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72c02-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72c02-126">OUTPUTS</span></span>

### <span data-ttu-id="72c02-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="72c02-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="72c02-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="72c02-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="72c02-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72c02-129">NOTES</span></span>
<span data-ttu-id="72c02-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="72c02-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="72c02-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72c02-131">RELATED LINKS</span></span>

