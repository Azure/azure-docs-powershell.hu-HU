---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 63c0184b9104b939073c4d58313777e8940d0f93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500011"
---
# <span data-ttu-id="5c7de-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="5c7de-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="5c7de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c7de-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7de-103">Lekérdezi egy vagy több kötelezettségvállalási társítás összefoglaló adatát.</span><span class="sxs-lookup"><span data-stu-id="5c7de-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c7de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c7de-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c7de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c7de-105">DESCRIPTION</span></span>
<span data-ttu-id="5c7de-106">Kikeresi a kötelezettségvállalási társítás adatait.</span><span class="sxs-lookup"><span data-stu-id="5c7de-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="5c7de-107">Az átadott paramenters függően a parancsmag egy adott kötelezettségvállalási társítást vagy a meghatározott kötelezettségvállalási csomaghoz tartozó kötelezettségvállalási társításokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5c7de-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="5c7de-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5c7de-108">EXAMPLES</span></span>

### <span data-ttu-id="5c7de-109">--------------------------Példa 1: speciális kötelezettségvállalási társítás beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="5c7de-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
<span data-ttu-id="5c7de-110">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5c7de-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="5c7de-111">--------------------------Példa 2: a meghatározott kötelezettségvállalási csomaghoz tartozó összes kötelezettségvállalási társítás beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="5c7de-111">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
<span data-ttu-id="5c7de-112">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5c7de-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="5c7de-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c7de-113">PARAMETERS</span></span>

### <span data-ttu-id="5c7de-114">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="5c7de-114">-CommitmentPlanName</span></span>
<span data-ttu-id="5c7de-115">Annak az Azure ML-ös kötelezettségvállalási csomagnak a neve, amely egy vagy több kötelezettségvállalási társítással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="5c7de-115">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="5c7de-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5c7de-116">-Name</span></span>
<span data-ttu-id="5c7de-117">Az Azure ML kötelezettségvállalási társítás neve.</span><span class="sxs-lookup"><span data-stu-id="5c7de-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="5c7de-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7de-118">-ResourceGroupName</span></span>
<span data-ttu-id="5c7de-119">Az Azure ML kötelezettségvállalási társítás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5c7de-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="5c7de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7de-120">-DefaultProfile</span></span>
<span data-ttu-id="5c7de-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c7de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c7de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7de-122">CommonParameters</span></span>
<span data-ttu-id="5c7de-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c7de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7de-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c7de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7de-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c7de-125">INPUTS</span></span>

## <span data-ttu-id="5c7de-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c7de-126">OUTPUTS</span></span>

### <span data-ttu-id="5c7de-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5c7de-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="5c7de-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="5c7de-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="5c7de-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c7de-129">NOTES</span></span>
<span data-ttu-id="5c7de-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="5c7de-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5c7de-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c7de-131">RELATED LINKS</span></span>

