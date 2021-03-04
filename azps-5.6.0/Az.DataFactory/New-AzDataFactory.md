---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: c13fdf46dff4ba0b62a8009bad7c4790507b2561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930121"
---
# <span data-ttu-id="fbd3a-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbd3a-101">New-AzDataFactory</span></span>

## <span data-ttu-id="fbd3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd3a-103">Adatüzemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-103">Creates a data factory.</span></span>

## <span data-ttu-id="fbd3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbd3a-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbd3a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="fbd3a-106">A **New-AzDataFactory** parancsmag létrehoz egy adatüzemet a megadott erőforráscsoport nevével és helyével.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="fbd3a-107">Ezeket a műveleteket a következő sorrendben végezze el:</span><span class="sxs-lookup"><span data-stu-id="fbd3a-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="fbd3a-108">Adatüzem létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbd3a-108">Create a data factory.</span></span> 
- <span data-ttu-id="fbd3a-109">Csatolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbd3a-109">Create linked services.</span></span> 
- <span data-ttu-id="fbd3a-110">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbd3a-110">Create datasets.</span></span> 
- <span data-ttu-id="fbd3a-111">Folyamat létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbd3a-111">Create a pipeline.</span></span>

## <span data-ttu-id="fbd3a-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbd3a-112">EXAMPLES</span></span>

### <span data-ttu-id="fbd3a-113">1. példa: Adat factory létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbd3a-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="fbd3a-114">Ez a parancs létrehoz egy WikiADF nevű adatüzemet az ADF nevű erőforráscsoportban a WestUS-helyen.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="fbd3a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbd3a-115">PARAMETERS</span></span>

### <span data-ttu-id="fbd3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd3a-116">-DefaultProfile</span></span>
<span data-ttu-id="fbd3a-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fbd3a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbd3a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fbd3a-118">-Force</span></span>
<span data-ttu-id="fbd3a-119">Azt jelzi, hogy ez a parancsmag egy meglévő adatüzemet vált fel megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fbd3a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="fbd3a-120">-Location</span></span>
<span data-ttu-id="fbd3a-121">Megadja az adat factory helyét, például a WestUS vagy az EastUS.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="fbd3a-122">Jelenleg csak a WestUS támogatott.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="fbd3a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fbd3a-123">-Name</span></span>
<span data-ttu-id="fbd3a-124">A létrehozni szükséges adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd3a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd3a-125">-ResourceGroupName</span></span>
<span data-ttu-id="fbd3a-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fbd3a-127">Ez a parancsmag létrehoz egy adatüzemet, amely a paraméter által megadott csoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbd3a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbd3a-128">-Tag</span></span>
<span data-ttu-id="fbd3a-129">Az adatüzem címkéi.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="fbd3a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbd3a-130">-Confirm</span></span>
<span data-ttu-id="fbd3a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbd3a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbd3a-132">-WhatIf</span></span>
<span data-ttu-id="fbd3a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbd3a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbd3a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd3a-135">CommonParameters</span></span>
<span data-ttu-id="fbd3a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbd3a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd3a-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbd3a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd3a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbd3a-138">INPUTS</span></span>

### <span data-ttu-id="fbd3a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fbd3a-139">System.String</span></span>

### <span data-ttu-id="fbd3a-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbd3a-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fbd3a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbd3a-141">OUTPUTS</span></span>

### <span data-ttu-id="fbd3a-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbd3a-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="fbd3a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbd3a-143">NOTES</span></span>
* <span data-ttu-id="fbd3a-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="fbd3a-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fbd3a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbd3a-145">RELATED LINKS</span></span>

[<span data-ttu-id="fbd3a-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbd3a-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="fbd3a-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbd3a-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


