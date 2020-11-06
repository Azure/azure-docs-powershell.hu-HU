---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: c1d6ae6c1396e23398bc1b52f4f32458999072a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497364"
---
# <span data-ttu-id="6cb09-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="6cb09-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="6cb09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cb09-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb09-103">Webes szolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="6cb09-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cb09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cb09-104">SYNTAX</span></span>

### <span data-ttu-id="6cb09-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cb09-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb09-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="6cb09-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb09-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cb09-107">DESCRIPTION</span></span>
<span data-ttu-id="6cb09-108">Egy erőforráscsoport által hivatkozott Azure Machine learning webszolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="6cb09-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="6cb09-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6cb09-109">EXAMPLES</span></span>

### <span data-ttu-id="6cb09-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6cb09-110">Example 1</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="6cb09-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cb09-111">PARAMETERS</span></span>

### <span data-ttu-id="6cb09-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb09-112">-DefaultProfile</span></span>
<span data-ttu-id="6cb09-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6cb09-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb09-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6cb09-114">-Force</span></span>
<span data-ttu-id="6cb09-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cb09-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6cb09-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="6cb09-116">-MlWebService</span></span>
<span data-ttu-id="6cb09-117">Az eltávolítandó webszolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="6cb09-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb09-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cb09-118">-Name</span></span>
<span data-ttu-id="6cb09-119">Az eltávolítandó webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="6cb09-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb09-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb09-120">-ResourceGroupName</span></span>
<span data-ttu-id="6cb09-121">A webszolgáltatás erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="6cb09-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb09-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cb09-122">-Confirm</span></span>
<span data-ttu-id="6cb09-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cb09-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb09-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb09-124">-WhatIf</span></span>
<span data-ttu-id="6cb09-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cb09-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb09-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cb09-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb09-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb09-127">CommonParameters</span></span>
<span data-ttu-id="6cb09-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cb09-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb09-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb09-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb09-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb09-130">INPUTS</span></span>

### <span data-ttu-id="6cb09-131">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="6cb09-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="6cb09-132">Paraméterek: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6cb09-132">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="6cb09-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb09-133">OUTPUTS</span></span>

### <span data-ttu-id="6cb09-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="6cb09-134">System.Void</span></span>

## <span data-ttu-id="6cb09-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cb09-135">NOTES</span></span>
<span data-ttu-id="6cb09-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="6cb09-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6cb09-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cb09-137">RELATED LINKS</span></span>
