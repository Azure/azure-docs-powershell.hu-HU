---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a0e8a131b0a66c3887ecea7054a2f13b75e7f598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667005"
---
# <span data-ttu-id="15e52-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="15e52-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="15e52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15e52-102">SYNOPSIS</span></span>
<span data-ttu-id="15e52-103">Egy kapcsolt szolgáltatás eltávolítása az Azure Data Factory alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="15e52-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="15e52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15e52-104">SYNTAX</span></span>

### <span data-ttu-id="15e52-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15e52-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15e52-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="15e52-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15e52-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="15e52-107">DESCRIPTION</span></span>
<span data-ttu-id="15e52-108">A **Remove-AzDataFactoryLinkedService** parancsmag egy kapcsolt szolgáltatást távolít el az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="15e52-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="15e52-109">Példák</span><span class="sxs-lookup"><span data-stu-id="15e52-109">EXAMPLES</span></span>

### <span data-ttu-id="15e52-110">1. példa: kapcsolt szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="15e52-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="15e52-111">Ez a parancs eltávolítja a LinkedServiceTest nevű kapcsolt szolgáltatást a WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="15e52-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="15e52-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="15e52-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="15e52-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15e52-113">PARAMETERS</span></span>

### <span data-ttu-id="15e52-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="15e52-114">-DataFactory</span></span>
<span data-ttu-id="15e52-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="15e52-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="15e52-116">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="15e52-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e52-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="15e52-117">-DataFactoryName</span></span>
<span data-ttu-id="15e52-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15e52-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="15e52-119">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="15e52-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e52-120">-DefaultProfile</span></span>
<span data-ttu-id="15e52-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15e52-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15e52-122">-Force</span><span class="sxs-lookup"><span data-stu-id="15e52-122">-Force</span></span>
<span data-ttu-id="15e52-123">Azt jelzi, hogy ez a parancsmag egy kapcsolt szolgáltatás eltávolítását követően nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15e52-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="15e52-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15e52-124">-Name</span></span>
<span data-ttu-id="15e52-125">Az eltávolítandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15e52-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e52-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e52-126">-ResourceGroupName</span></span>
<span data-ttu-id="15e52-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15e52-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="15e52-128">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="15e52-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e52-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15e52-129">-Confirm</span></span>
<span data-ttu-id="15e52-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15e52-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e52-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e52-131">-WhatIf</span></span>
<span data-ttu-id="15e52-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15e52-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15e52-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15e52-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e52-134">CommonParameters</span></span>
<span data-ttu-id="15e52-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15e52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e52-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e52-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e52-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15e52-137">INPUTS</span></span>

### <span data-ttu-id="15e52-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="15e52-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="15e52-139">System. String</span><span class="sxs-lookup"><span data-stu-id="15e52-139">System.String</span></span>

## <span data-ttu-id="15e52-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15e52-140">OUTPUTS</span></span>

### <span data-ttu-id="15e52-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="15e52-141">System.Void</span></span>

## <span data-ttu-id="15e52-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15e52-142">NOTES</span></span>
* <span data-ttu-id="15e52-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="15e52-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="15e52-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15e52-144">RELATED LINKS</span></span>

[<span data-ttu-id="15e52-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="15e52-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="15e52-146">Új – AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="15e52-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


