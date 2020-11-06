---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8dc191223d5ec17856605c7640d324cc2ee3794e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505980"
---
# <span data-ttu-id="846d9-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="846d9-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="846d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="846d9-102">SYNOPSIS</span></span>
<span data-ttu-id="846d9-103">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="846d9-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="846d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="846d9-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
[[-Tag] <Hashtable>] [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="846d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="846d9-105">DESCRIPTION</span></span>
<span data-ttu-id="846d9-106">A **set-AzureRmDataFactoryV2** parancsmag adatfeldolgozót hoz létre a megadott erőforráscsoport-névvel és-hellyel.</span><span class="sxs-lookup"><span data-stu-id="846d9-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="846d9-107">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="846d9-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="846d9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="846d9-108">EXAMPLES</span></span>

### <span data-ttu-id="846d9-109">Példa 1: adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="846d9-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="846d9-110">Ez a parancs létrehoz egy WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport WestUS helyéről.</span><span class="sxs-lookup"><span data-stu-id="846d9-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="846d9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="846d9-111">PARAMETERS</span></span>

### <span data-ttu-id="846d9-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="846d9-112">-Confirm</span></span>
<span data-ttu-id="846d9-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="846d9-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846d9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="846d9-114">-Force</span></span>
<span data-ttu-id="846d9-115">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="846d9-115">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="846d9-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="846d9-116">-Location</span></span>
<span data-ttu-id="846d9-117">Az adatfeldolgozó ebben a régióban jön létre.</span><span class="sxs-lookup"><span data-stu-id="846d9-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846d9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="846d9-118">-Name</span></span>
<span data-ttu-id="846d9-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="846d9-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="846d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="846d9-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="846d9-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846d9-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="846d9-122">-Tag</span></span>
<span data-ttu-id="846d9-123">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="846d9-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="846d9-124">-WhatIf</span></span>
<span data-ttu-id="846d9-125">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="846d9-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="846d9-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="846d9-126">INPUTS</span></span>

### <span data-ttu-id="846d9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="846d9-127">System.String</span></span>
<span data-ttu-id="846d9-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="846d9-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="846d9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="846d9-129">OUTPUTS</span></span>

### <span data-ttu-id="846d9-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="846d9-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="846d9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="846d9-131">NOTES</span></span>
<span data-ttu-id="846d9-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="846d9-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="846d9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="846d9-133">RELATED LINKS</span></span>
[<span data-ttu-id="846d9-134">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="846d9-134">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="846d9-135">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="846d9-135">Remove-AzureRmDataFactoryV2</span></span>]()
