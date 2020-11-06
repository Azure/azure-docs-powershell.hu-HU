---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500004"
---
# <span data-ttu-id="3c1db-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="3c1db-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="3c1db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c1db-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1db-103">Webes szolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="3c1db-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c1db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c1db-104">SYNTAX</span></span>

### <span data-ttu-id="3c1db-105">Azure ML webszolgáltatás Resouce eltávolítása név és erőforráscsoport szerint</span><span class="sxs-lookup"><span data-stu-id="3c1db-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c1db-106">Objektumként megadott Azure ML-webszolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3c1db-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c1db-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c1db-107">DESCRIPTION</span></span>
<span data-ttu-id="3c1db-108">Egy erőforráscsoport által hivatkozott Azure Machine learning webszolgáltatás törlése</span><span class="sxs-lookup"><span data-stu-id="3c1db-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="3c1db-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3c1db-109">EXAMPLES</span></span>

### <span data-ttu-id="3c1db-110">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c1db-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="3c1db-111">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3c1db-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="3c1db-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c1db-112">PARAMETERS</span></span>

### <span data-ttu-id="3c1db-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3c1db-113">-Force</span></span>
<span data-ttu-id="3c1db-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c1db-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3c1db-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="3c1db-115">-MlWebService</span></span>
<span data-ttu-id="3c1db-116">Az eltávolítandó webszolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="3c1db-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1db-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c1db-117">-Name</span></span>
<span data-ttu-id="3c1db-118">Az eltávolítandó webszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3c1db-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1db-119">-ResourceGroupName</span></span>
<span data-ttu-id="3c1db-120">A webszolgáltatás erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="3c1db-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1db-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c1db-121">-Confirm</span></span>
<span data-ttu-id="3c1db-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c1db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c1db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c1db-123">-WhatIf</span></span>
<span data-ttu-id="3c1db-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c1db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c1db-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c1db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c1db-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1db-126">-DefaultProfile</span></span>
<span data-ttu-id="3c1db-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c1db-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c1db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1db-128">CommonParameters</span></span>
<span data-ttu-id="3c1db-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c1db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1db-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c1db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1db-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c1db-131">INPUTS</span></span>

### <span data-ttu-id="3c1db-132">WebService</span><span class="sxs-lookup"><span data-stu-id="3c1db-132">WebService</span></span>
<span data-ttu-id="3c1db-133">A ' MlWebService ' paraméter a "webszolgáltatás" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3c1db-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="3c1db-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c1db-134">OUTPUTS</span></span>

### <span data-ttu-id="3c1db-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="3c1db-135">None</span></span>

## <span data-ttu-id="3c1db-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c1db-136">NOTES</span></span>
<span data-ttu-id="3c1db-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="3c1db-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3c1db-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c1db-138">RELATED LINKS</span></span>

