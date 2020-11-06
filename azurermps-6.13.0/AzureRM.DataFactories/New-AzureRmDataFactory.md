---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 1636dd6b101a7639c84b0cd7c2659eac23a10b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503003"
---
# <span data-ttu-id="474d4-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="474d4-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="474d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="474d4-102">SYNOPSIS</span></span>
<span data-ttu-id="474d4-103">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="474d4-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="474d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="474d4-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="474d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="474d4-105">DESCRIPTION</span></span>
<span data-ttu-id="474d4-106">A **New-AzureRmDataFactory** parancsmag létrehoz egy adatfeldolgozót a megadott erőforráscsoport nevével és helyével.</span><span class="sxs-lookup"><span data-stu-id="474d4-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="474d4-107">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="474d4-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="474d4-108">Adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="474d4-108">Create a data factory.</span></span> 
- <span data-ttu-id="474d4-109">Kapcsolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="474d4-109">Create linked services.</span></span> 
- <span data-ttu-id="474d4-110">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="474d4-110">Create datasets.</span></span> 
- <span data-ttu-id="474d4-111">Csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="474d4-111">Create a pipeline.</span></span>

## <span data-ttu-id="474d4-112">Példák</span><span class="sxs-lookup"><span data-stu-id="474d4-112">EXAMPLES</span></span>

### <span data-ttu-id="474d4-113">Példa 1: adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="474d4-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="474d4-114">Ez a parancs létrehoz egy WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport WestUS helyéről.</span><span class="sxs-lookup"><span data-stu-id="474d4-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="474d4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="474d4-115">PARAMETERS</span></span>

### <span data-ttu-id="474d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474d4-116">-DefaultProfile</span></span>
<span data-ttu-id="474d4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="474d4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="474d4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="474d4-118">-Force</span></span>
<span data-ttu-id="474d4-119">Azt jelzi, hogy ez a parancsmag egy meglévő adattárolót cserél, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="474d4-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="474d4-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="474d4-120">-Location</span></span>
<span data-ttu-id="474d4-121">Az adatfeldolgozó helyét adja meg, például WestUS vagy EastUS.</span><span class="sxs-lookup"><span data-stu-id="474d4-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="474d4-122">Jelenleg csak a WestUS támogatott.</span><span class="sxs-lookup"><span data-stu-id="474d4-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="474d4-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="474d4-123">-Name</span></span>
<span data-ttu-id="474d4-124">A létrehozandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="474d4-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="474d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="474d4-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="474d4-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="474d4-127">Ez a parancsmag olyan adattípust hoz létre, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="474d4-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="474d4-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="474d4-128">-Tag</span></span>
<span data-ttu-id="474d4-129">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="474d4-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="474d4-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="474d4-130">-Confirm</span></span>
<span data-ttu-id="474d4-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="474d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="474d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="474d4-132">-WhatIf</span></span>
<span data-ttu-id="474d4-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="474d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="474d4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="474d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="474d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474d4-135">CommonParameters</span></span>
<span data-ttu-id="474d4-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="474d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474d4-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474d4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474d4-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="474d4-138">INPUTS</span></span>

### <span data-ttu-id="474d4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="474d4-139">System.String</span></span>

### <span data-ttu-id="474d4-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="474d4-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="474d4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="474d4-141">OUTPUTS</span></span>

### <span data-ttu-id="474d4-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="474d4-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="474d4-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="474d4-143">NOTES</span></span>
* <span data-ttu-id="474d4-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="474d4-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="474d4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="474d4-145">RELATED LINKS</span></span>

[<span data-ttu-id="474d4-146">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="474d4-146">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="474d4-147">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="474d4-147">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


