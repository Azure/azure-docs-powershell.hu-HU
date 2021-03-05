---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 46e9ae8f4b6b4bb954bca158adb82c0d821d67eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006694"
---
# <span data-ttu-id="9c14e-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="9c14e-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="9c14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c14e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c14e-103">Webszolgáltatás törlése.</span><span class="sxs-lookup"><span data-stu-id="9c14e-103">Deletes a web service.</span></span>

## <span data-ttu-id="9c14e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c14e-104">SYNTAX</span></span>

### <span data-ttu-id="9c14e-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c14e-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c14e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9c14e-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c14e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c14e-107">DESCRIPTION</span></span>
<span data-ttu-id="9c14e-108">Törli az erőforráscsoport és a név alapján hivatkozott Azure Machine Learning webszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="9c14e-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="9c14e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c14e-109">EXAMPLES</span></span>

### <span data-ttu-id="9c14e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9c14e-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="9c14e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c14e-111">PARAMETERS</span></span>

### <span data-ttu-id="9c14e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c14e-112">-DefaultProfile</span></span>
<span data-ttu-id="9c14e-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9c14e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c14e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9c14e-114">-Force</span></span>
<span data-ttu-id="9c14e-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c14e-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9c14e-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="9c14e-116">-MlWebService</span></span>
<span data-ttu-id="9c14e-117">Az eltávolítható webszolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="9c14e-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="9c14e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9c14e-118">-Name</span></span>
<span data-ttu-id="9c14e-119">Az eltávolítható webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="9c14e-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="9c14e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c14e-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c14e-121">A webszolgáltatás erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="9c14e-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="9c14e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c14e-122">-Confirm</span></span>
<span data-ttu-id="9c14e-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9c14e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c14e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c14e-124">-WhatIf</span></span>
<span data-ttu-id="9c14e-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9c14e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c14e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c14e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c14e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c14e-127">CommonParameters</span></span>
<span data-ttu-id="9c14e-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c14e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c14e-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c14e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c14e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c14e-130">INPUTS</span></span>

### <span data-ttu-id="9c14e-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="9c14e-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="9c14e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c14e-132">OUTPUTS</span></span>

### <span data-ttu-id="9c14e-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="9c14e-133">System.Void</span></span>

## <span data-ttu-id="9c14e-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c14e-134">NOTES</span></span>
<span data-ttu-id="9c14e-135">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="9c14e-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9c14e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c14e-136">RELATED LINKS</span></span>
