---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 24f12a0e95ab7c233a08ec1ad0f4dc330583dd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505900"
---
# <span data-ttu-id="40052-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="40052-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="40052-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40052-102">SYNOPSIS</span></span>
<span data-ttu-id="40052-103">Helyi webszolgáltatás-tulajdonságokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="40052-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40052-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40052-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40052-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40052-105">DESCRIPTION</span></span>
<span data-ttu-id="40052-106">Azure Machine learning területi tulajdonságainak létrehozása meglévő webszolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="40052-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="40052-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40052-107">EXAMPLES</span></span>

### <span data-ttu-id="40052-108">--------------------------Példa 1: új területi tulajdonságok felvétele a Nyugat-Közép-amerikai--------------------------</span><span class="sxs-lookup"><span data-stu-id="40052-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>
<span data-ttu-id="40052-109">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="40052-109">@{paragraph=PS C:\\\>}</span></span>



```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="40052-110">A példaként létrehozott parancs a "Nyugat-Közép-amerikai" régióban létrehoz egy webszolgáltatás területi tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="40052-110">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="40052-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40052-111">PARAMETERS</span></span>

### <span data-ttu-id="40052-112">-Force</span><span class="sxs-lookup"><span data-stu-id="40052-112">-Force</span></span>
<span data-ttu-id="40052-113">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40052-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="40052-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40052-114">-Name</span></span>
<span data-ttu-id="40052-115">A webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="40052-115">The name for the web service.</span></span>

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

### <span data-ttu-id="40052-116">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="40052-116">-Region</span></span>
<span data-ttu-id="40052-117">Az a terület, ahol a webszolgáltatás tulajdonságait létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="40052-117">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="40052-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40052-118">-ResourceGroupName</span></span>
<span data-ttu-id="40052-119">Az erőforráscsoport, amelyben a webszolgáltatás tartozik.</span><span class="sxs-lookup"><span data-stu-id="40052-119">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="40052-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40052-120">-Confirm</span></span>
<span data-ttu-id="40052-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40052-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40052-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40052-122">-WhatIf</span></span>
<span data-ttu-id="40052-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40052-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40052-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40052-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40052-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40052-125">-DefaultProfile</span></span>
<span data-ttu-id="40052-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40052-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40052-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40052-127">CommonParameters</span></span>
<span data-ttu-id="40052-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40052-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40052-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40052-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40052-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40052-130">INPUTS</span></span>

## <span data-ttu-id="40052-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40052-131">OUTPUTS</span></span>

### <span data-ttu-id="40052-132">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="40052-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="40052-133">Az Azure Machine learning webszolgáltatás összefoglaló leírása.</span><span class="sxs-lookup"><span data-stu-id="40052-133">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="40052-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40052-134">NOTES</span></span>
<span data-ttu-id="40052-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="40052-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="40052-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40052-136">RELATED LINKS</span></span>

