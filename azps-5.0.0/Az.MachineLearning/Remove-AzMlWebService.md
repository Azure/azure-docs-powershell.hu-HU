---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194633"
---
# <span data-ttu-id="97793-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="97793-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="97793-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97793-102">SYNOPSIS</span></span>
<span data-ttu-id="97793-103">Webes szolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="97793-103">Deletes a web service.</span></span>

## <span data-ttu-id="97793-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97793-104">SYNTAX</span></span>

### <span data-ttu-id="97793-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="97793-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97793-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="97793-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97793-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="97793-107">DESCRIPTION</span></span>
<span data-ttu-id="97793-108">Egy erőforráscsoport által hivatkozott Azure Machine learning webszolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="97793-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="97793-109">Példák</span><span class="sxs-lookup"><span data-stu-id="97793-109">EXAMPLES</span></span>

### <span data-ttu-id="97793-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97793-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="97793-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97793-111">PARAMETERS</span></span>

### <span data-ttu-id="97793-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97793-112">-DefaultProfile</span></span>
<span data-ttu-id="97793-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97793-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97793-114">-Force</span><span class="sxs-lookup"><span data-stu-id="97793-114">-Force</span></span>
<span data-ttu-id="97793-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97793-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="97793-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="97793-116">-MlWebService</span></span>
<span data-ttu-id="97793-117">Az eltávolítandó webszolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="97793-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="97793-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97793-118">-Name</span></span>
<span data-ttu-id="97793-119">Az eltávolítandó webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="97793-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="97793-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97793-120">-ResourceGroupName</span></span>
<span data-ttu-id="97793-121">A webszolgáltatás erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="97793-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="97793-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97793-122">-Confirm</span></span>
<span data-ttu-id="97793-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97793-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97793-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97793-124">-WhatIf</span></span>
<span data-ttu-id="97793-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97793-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97793-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97793-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97793-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97793-127">CommonParameters</span></span>
<span data-ttu-id="97793-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97793-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97793-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97793-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97793-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97793-130">INPUTS</span></span>

### <span data-ttu-id="97793-131">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="97793-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="97793-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97793-132">OUTPUTS</span></span>

### <span data-ttu-id="97793-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="97793-133">System.Void</span></span>

## <span data-ttu-id="97793-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97793-134">NOTES</span></span>
<span data-ttu-id="97793-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="97793-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="97793-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97793-136">RELATED LINKS</span></span>
