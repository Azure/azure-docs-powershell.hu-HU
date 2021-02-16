---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157538"
---
# <span data-ttu-id="149b4-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="149b4-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="149b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="149b4-102">SYNOPSIS</span></span>
<span data-ttu-id="149b4-103">Területi webszolgáltatás-tulajdonságokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="149b4-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="149b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="149b4-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="149b4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="149b4-105">DESCRIPTION</span></span>
<span data-ttu-id="149b4-106">Azure Machine Learning regionális tulajdonságokat hoz létre egy meglévő webszolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="149b4-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="149b4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="149b4-107">EXAMPLES</span></span>

### <span data-ttu-id="149b4-108">1. példa: Új regionális tulajdonságok hozzáadása az EGYESÜLT Egyesült Régió régióhoz</span><span class="sxs-lookup"><span data-stu-id="149b4-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="149b4-109">Ez a példaparancs egy webszolgáltatás regionális tulajdonságát hozza létre az "Egyesült Államok nyugati részén"</span><span class="sxs-lookup"><span data-stu-id="149b4-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="149b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="149b4-110">PARAMETERS</span></span>

### <span data-ttu-id="149b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149b4-111">-DefaultProfile</span></span>
<span data-ttu-id="149b4-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="149b4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="149b4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="149b4-113">-Force</span></span>
<span data-ttu-id="149b4-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="149b4-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="149b4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="149b4-115">-Name</span></span>
<span data-ttu-id="149b4-116">A webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="149b4-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="149b4-117">-Régió</span><span class="sxs-lookup"><span data-stu-id="149b4-117">-Region</span></span>
<span data-ttu-id="149b4-118">Az a régió, amelyben létre kell hoznia a webszolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="149b4-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="149b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="149b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="149b4-120">Az az erőforráscsoport, amelyhez a webszolgáltatás tartozik.</span><span class="sxs-lookup"><span data-stu-id="149b4-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="149b4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="149b4-121">-Confirm</span></span>
<span data-ttu-id="149b4-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="149b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="149b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="149b4-123">-WhatIf</span></span>
<span data-ttu-id="149b4-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="149b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="149b4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="149b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="149b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149b4-126">CommonParameters</span></span>
<span data-ttu-id="149b4-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="149b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149b4-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="149b4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149b4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="149b4-129">INPUTS</span></span>

### <span data-ttu-id="149b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="149b4-130">System.String</span></span>

## <span data-ttu-id="149b4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="149b4-131">OUTPUTS</span></span>

### <span data-ttu-id="149b4-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="149b4-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="149b4-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="149b4-133">NOTES</span></span>
<span data-ttu-id="149b4-134">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="149b4-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="149b4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="149b4-135">RELATED LINKS</span></span>
