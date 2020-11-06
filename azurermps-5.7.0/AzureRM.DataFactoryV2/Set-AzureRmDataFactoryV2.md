---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: f0fcfd8a99bd28f01077257e48c0dc9662973751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492296"
---
# <span data-ttu-id="a36d4-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a36d4-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="a36d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a36d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a36d4-103">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a36d4-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a36d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a36d4-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a36d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a36d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a36d4-106">A **set-AzureRmDataFactoryV2** parancsmag adatfeldolgozót hoz létre a megadott erőforráscsoport-névvel és-hellyel.</span><span class="sxs-lookup"><span data-stu-id="a36d4-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="a36d4-107">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="a36d4-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="a36d4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a36d4-108">EXAMPLES</span></span>

### <span data-ttu-id="a36d4-109">Példa 1: adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="a36d4-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="a36d4-110">Ez a parancs létrehoz egy WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport WestUS helyéről.</span><span class="sxs-lookup"><span data-stu-id="a36d4-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="a36d4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a36d4-111">PARAMETERS</span></span>

### <span data-ttu-id="a36d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36d4-112">-DefaultProfile</span></span>
<span data-ttu-id="a36d4-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a36d4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36d4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a36d4-114">-Force</span></span>
<span data-ttu-id="a36d4-115">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a36d4-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a36d4-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="a36d4-116">-Location</span></span>
<span data-ttu-id="a36d4-117">Az adatfeldolgozó ebben a régióban jön létre.</span><span class="sxs-lookup"><span data-stu-id="a36d4-117">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="a36d4-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a36d4-118">-Name</span></span>
<span data-ttu-id="a36d4-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="a36d4-119">The data factory name.</span></span>

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

### <span data-ttu-id="a36d4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a36d4-120">-ResourceGroupName</span></span>
<span data-ttu-id="a36d4-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a36d4-121">The resource group name.</span></span>

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

### <span data-ttu-id="a36d4-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="a36d4-122">-Tag</span></span>
<span data-ttu-id="a36d4-123">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="a36d4-123">The tags of the data factory.</span></span>

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

### <span data-ttu-id="a36d4-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a36d4-124">-Confirm</span></span>
<span data-ttu-id="a36d4-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a36d4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a36d4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a36d4-126">-WhatIf</span></span>
<span data-ttu-id="a36d4-127">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a36d4-127">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a36d4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36d4-128">CommonParameters</span></span>
<span data-ttu-id="a36d4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a36d4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36d4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a36d4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36d4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a36d4-131">INPUTS</span></span>

### <span data-ttu-id="a36d4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a36d4-132">System.String</span></span>
<span data-ttu-id="a36d4-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a36d4-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a36d4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a36d4-134">OUTPUTS</span></span>

### <span data-ttu-id="a36d4-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a36d4-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a36d4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a36d4-136">NOTES</span></span>
<span data-ttu-id="a36d4-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="a36d4-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a36d4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a36d4-138">RELATED LINKS</span></span>

[<span data-ttu-id="a36d4-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a36d4-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="a36d4-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a36d4-140">Remove-AzureRmDataFactoryV2</span></span>]()
