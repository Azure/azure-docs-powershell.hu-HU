---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d2745a0dd73141c1da7d049494e3a1545ee92599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503603"
---
# <span data-ttu-id="4efb4-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4efb4-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="4efb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4efb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4efb4-103">Új kötelezettségvállalási terv létrehozása.</span><span class="sxs-lookup"><span data-stu-id="4efb4-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4efb4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4efb4-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4efb4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4efb4-105">DESCRIPTION</span></span>
<span data-ttu-id="4efb4-106">Azure Machine learning kötelezettségvállalási terv létrehozása egy meglévő erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="4efb4-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="4efb4-107">Ha az erőforráscsoport azonos nevű kötelezettségvállalási terve létezik, a hívás frissítési műveletként működik, és a meglévő kötelezettségvállalási terv felülíródik.</span><span class="sxs-lookup"><span data-stu-id="4efb4-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="4efb4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4efb4-108">EXAMPLES</span></span>

### <span data-ttu-id="4efb4-109">Példa 1: új kötelezettségvállalási terv létrehozása</span><span class="sxs-lookup"><span data-stu-id="4efb4-109">Example 1: Create a new commitment plan</span></span>
```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="4efb4-110">Új Azure Machine learning kötelezettségvállalási csomagot hoz létre "MyCommitmentPlanName" néven a "MyResourceGroup" csoportban és Dél-Közép-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="4efb4-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="4efb4-111">Ebben a példában az SKU DevTest/standard használatos, vagyis a kötelezettségvállalási terv által biztosított erőforrásokat a DevTest/standard korlátai határozzák meg.</span><span class="sxs-lookup"><span data-stu-id="4efb4-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="4efb4-112">Ebben a példában a SkuCapacity 1, vagyis a terv költsége a DevTest költségét fogja tartalmazni, és a terv tartalma 1x lesz, amit a DevTest tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4efb4-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="4efb4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4efb4-113">PARAMETERS</span></span>

### <span data-ttu-id="4efb4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efb4-114">-DefaultProfile</span></span>
<span data-ttu-id="4efb4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4efb4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4efb4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4efb4-116">-Force</span></span>
<span data-ttu-id="4efb4-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4efb4-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efb4-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="4efb4-118">-Location</span></span>
<span data-ttu-id="4efb4-119">Az Azure ML kötelezettségvállalási csomag helye.</span><span class="sxs-lookup"><span data-stu-id="4efb4-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4efb4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4efb4-120">-Name</span></span>
<span data-ttu-id="4efb4-121">Az Azure ML kötelezettségvállalási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="4efb4-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4efb4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4efb4-122">-ResourceGroupName</span></span>
<span data-ttu-id="4efb4-123">Az Azure ML kötelezettségvállalási csomag erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4efb4-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4efb4-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4efb4-124">-SkuCapacity</span></span>
<span data-ttu-id="4efb4-125">Az az SKU kapacitása, amelyet az Azure ML kötelezettségvállalási csomag kiépítésekor kell használni.</span><span class="sxs-lookup"><span data-stu-id="4efb4-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efb4-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4efb4-126">-SkuName</span></span>
<span data-ttu-id="4efb4-127">Az Azure ML kötelezettségvállalási csomag kiépítésekor használandó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="4efb4-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4efb4-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4efb4-128">-SkuTier</span></span>
<span data-ttu-id="4efb4-129">Az az adatsku-szint, amelyet az Azure ML kötelezettségvállalási csomag kiépítésekor kell használni.</span><span class="sxs-lookup"><span data-stu-id="4efb4-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4efb4-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4efb4-130">-Confirm</span></span>
<span data-ttu-id="4efb4-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4efb4-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efb4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4efb4-132">-WhatIf</span></span>
<span data-ttu-id="4efb4-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4efb4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4efb4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4efb4-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efb4-135">CommonParameters</span></span>
<span data-ttu-id="4efb4-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4efb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efb4-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4efb4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efb4-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4efb4-138">INPUTS</span></span>

### <span data-ttu-id="4efb4-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="4efb4-139">None</span></span>

## <span data-ttu-id="4efb4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4efb4-140">OUTPUTS</span></span>

### <span data-ttu-id="4efb4-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4efb4-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="4efb4-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4efb4-142">NOTES</span></span>
<span data-ttu-id="4efb4-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="4efb4-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4efb4-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4efb4-144">RELATED LINKS</span></span>
