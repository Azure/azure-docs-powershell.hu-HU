---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496260"
---
# <span data-ttu-id="f5ea7-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f5ea7-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="f5ea7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ea7-103">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5ea7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5ea7-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5ea7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ea7-106">A **set-AzureRmDataFactoryV2** parancsmag adatfeldolgozót hoz létre a megadott erőforráscsoport-névvel és-hellyel.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="f5ea7-107">Végezze el ezeket a műveleteket a következő sorrendben:-------hoz létre egy adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="f5ea7-108">– Kapcsolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-108">-- Create linked services.</span></span>
<span data-ttu-id="f5ea7-109">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-109">-- Create datasets.</span></span>
<span data-ttu-id="f5ea7-110">– Csővezeték létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="f5ea7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f5ea7-111">EXAMPLES</span></span>

### <span data-ttu-id="f5ea7-112">Példa 1: adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5ea7-112">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="f5ea7-113">Ez a parancs létrehoz egy WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport WestUS helyéről.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="f5ea7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5ea7-114">PARAMETERS</span></span>

### <span data-ttu-id="f5ea7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ea7-115">-DefaultProfile</span></span>
<span data-ttu-id="f5ea7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5ea7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f5ea7-117">-Force</span></span>
<span data-ttu-id="f5ea7-118">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f5ea7-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="f5ea7-119">-Location</span></span>
<span data-ttu-id="f5ea7-120">Az adatfeldolgozó ebben a régióban jön létre.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-120">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ea7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5ea7-121">-Name</span></span>
<span data-ttu-id="f5ea7-122">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-122">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ea7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ea7-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5ea7-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ea7-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="f5ea7-125">-Tag</span></span>
<span data-ttu-id="f5ea7-126">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-126">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ea7-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5ea7-127">-Confirm</span></span>
<span data-ttu-id="f5ea7-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ea7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ea7-129">-WhatIf</span></span>
<span data-ttu-id="f5ea7-130">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f5ea7-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f5ea7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ea7-131">CommonParameters</span></span>
<span data-ttu-id="f5ea7-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5ea7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ea7-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ea7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ea7-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ea7-134">INPUTS</span></span>

### <span data-ttu-id="f5ea7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f5ea7-135">System.String</span></span>

### <span data-ttu-id="f5ea7-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f5ea7-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f5ea7-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ea7-137">OUTPUTS</span></span>

### <span data-ttu-id="f5ea7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f5ea7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f5ea7-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5ea7-139">NOTES</span></span>
<span data-ttu-id="f5ea7-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="f5ea7-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5ea7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5ea7-141">RELATED LINKS</span></span>

[<span data-ttu-id="f5ea7-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f5ea7-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="f5ea7-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f5ea7-143">Remove-AzureRmDataFactoryV2</span></span>]()
