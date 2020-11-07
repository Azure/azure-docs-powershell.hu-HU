---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847238"
---
# <span data-ttu-id="804f6-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="804f6-101">New-AzDataFactory</span></span>

## <span data-ttu-id="804f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="804f6-102">SYNOPSIS</span></span>
<span data-ttu-id="804f6-103">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="804f6-103">Creates a data factory.</span></span>

## <span data-ttu-id="804f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="804f6-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="804f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="804f6-105">DESCRIPTION</span></span>
<span data-ttu-id="804f6-106">A **New-AzDataFactory** parancsmag létrehoz egy adatfeldolgozót a megadott erőforráscsoport nevével és helyével.</span><span class="sxs-lookup"><span data-stu-id="804f6-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="804f6-107">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="804f6-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="804f6-108">Adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="804f6-108">Create a data factory.</span></span> 
- <span data-ttu-id="804f6-109">Kapcsolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="804f6-109">Create linked services.</span></span> 
- <span data-ttu-id="804f6-110">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="804f6-110">Create datasets.</span></span> 
- <span data-ttu-id="804f6-111">Csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="804f6-111">Create a pipeline.</span></span>

## <span data-ttu-id="804f6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="804f6-112">EXAMPLES</span></span>

### <span data-ttu-id="804f6-113">Példa 1: adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="804f6-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="804f6-114">Ez a parancs létrehoz egy WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport WestUS helyéről.</span><span class="sxs-lookup"><span data-stu-id="804f6-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="804f6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="804f6-115">PARAMETERS</span></span>

### <span data-ttu-id="804f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804f6-116">-DefaultProfile</span></span>
<span data-ttu-id="804f6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="804f6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="804f6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="804f6-118">-Force</span></span>
<span data-ttu-id="804f6-119">Azt jelzi, hogy ez a parancsmag egy meglévő adattárolót cserél, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="804f6-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="804f6-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="804f6-120">-Location</span></span>
<span data-ttu-id="804f6-121">Az adatfeldolgozó helyét adja meg, például WestUS vagy EastUS.</span><span class="sxs-lookup"><span data-stu-id="804f6-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="804f6-122">Jelenleg csak a WestUS támogatott.</span><span class="sxs-lookup"><span data-stu-id="804f6-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="804f6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="804f6-123">-Name</span></span>
<span data-ttu-id="804f6-124">A létrehozandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="804f6-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="804f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="804f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="804f6-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="804f6-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="804f6-127">Ez a parancsmag olyan adattípust hoz létre, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="804f6-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="804f6-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="804f6-128">-Tag</span></span>
<span data-ttu-id="804f6-129">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="804f6-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="804f6-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="804f6-130">-Confirm</span></span>
<span data-ttu-id="804f6-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="804f6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="804f6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="804f6-132">-WhatIf</span></span>
<span data-ttu-id="804f6-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="804f6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="804f6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="804f6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="804f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804f6-135">CommonParameters</span></span>
<span data-ttu-id="804f6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="804f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804f6-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804f6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804f6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="804f6-138">INPUTS</span></span>

### <span data-ttu-id="804f6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="804f6-139">System.String</span></span>

### <span data-ttu-id="804f6-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="804f6-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="804f6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="804f6-141">OUTPUTS</span></span>

### <span data-ttu-id="804f6-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="804f6-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="804f6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="804f6-143">NOTES</span></span>
* <span data-ttu-id="804f6-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="804f6-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="804f6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="804f6-145">RELATED LINKS</span></span>

[<span data-ttu-id="804f6-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="804f6-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="804f6-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="804f6-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)

