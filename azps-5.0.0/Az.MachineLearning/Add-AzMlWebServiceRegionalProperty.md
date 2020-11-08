---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194651"
---
# <span data-ttu-id="47213-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="47213-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="47213-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47213-102">SYNOPSIS</span></span>
<span data-ttu-id="47213-103">Helyi webszolgáltatás-tulajdonságokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47213-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="47213-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47213-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47213-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47213-105">DESCRIPTION</span></span>
<span data-ttu-id="47213-106">Azure Machine learning területi tulajdonságainak létrehozása meglévő webszolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="47213-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="47213-107">Példák</span><span class="sxs-lookup"><span data-stu-id="47213-107">EXAMPLES</span></span>

### <span data-ttu-id="47213-108">1. példa: új területi tulajdonságok felvétele a közép-amerikai nyugaton</span><span class="sxs-lookup"><span data-stu-id="47213-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="47213-109">A példaként létrehozott parancs a "Nyugat-Közép-amerikai" régióban létrehoz egy webszolgáltatás területi tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="47213-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="47213-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47213-110">PARAMETERS</span></span>

### <span data-ttu-id="47213-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47213-111">-DefaultProfile</span></span>
<span data-ttu-id="47213-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="47213-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47213-113">-Force</span><span class="sxs-lookup"><span data-stu-id="47213-113">-Force</span></span>
<span data-ttu-id="47213-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47213-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47213-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47213-115">-Name</span></span>
<span data-ttu-id="47213-116">A webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="47213-116">The name for the web service.</span></span>

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

### <span data-ttu-id="47213-117">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="47213-117">-Region</span></span>
<span data-ttu-id="47213-118">Az a terület, ahol a webszolgáltatás tulajdonságait létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="47213-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="47213-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47213-119">-ResourceGroupName</span></span>
<span data-ttu-id="47213-120">Az erőforráscsoport, amelyben a webszolgáltatás tartozik.</span><span class="sxs-lookup"><span data-stu-id="47213-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="47213-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47213-121">-Confirm</span></span>
<span data-ttu-id="47213-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47213-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47213-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47213-123">-WhatIf</span></span>
<span data-ttu-id="47213-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47213-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47213-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47213-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47213-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47213-126">CommonParameters</span></span>
<span data-ttu-id="47213-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47213-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47213-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47213-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47213-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47213-129">INPUTS</span></span>

### <span data-ttu-id="47213-130">System. String</span><span class="sxs-lookup"><span data-stu-id="47213-130">System.String</span></span>

## <span data-ttu-id="47213-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47213-131">OUTPUTS</span></span>

### <span data-ttu-id="47213-132">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="47213-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="47213-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47213-133">NOTES</span></span>
<span data-ttu-id="47213-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="47213-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="47213-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47213-135">RELATED LINKS</span></span>