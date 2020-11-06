---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 13e9a8de97ee19e53c31a76516fef7c9fcfcaedd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492489"
---
# <span data-ttu-id="71965-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="71965-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="71965-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71965-102">SYNOPSIS</span></span>
<span data-ttu-id="71965-103">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="71965-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71965-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71965-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tags] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71965-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71965-105">DESCRIPTION</span></span>
<span data-ttu-id="71965-106">A **New-AzureRmDataFactory** parancsmag létrehoz egy adatfeldolgozót a megadott erőforráscsoport nevével és helyével.</span><span class="sxs-lookup"><span data-stu-id="71965-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="71965-107">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="71965-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="71965-108">Adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="71965-108">Create a data factory.</span></span> 
- <span data-ttu-id="71965-109">Kapcsolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="71965-109">Create linked services.</span></span> 
- <span data-ttu-id="71965-110">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="71965-110">Create datasets.</span></span> 
- <span data-ttu-id="71965-111">Csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="71965-111">Create a pipeline.</span></span>

## <span data-ttu-id="71965-112">Példák</span><span class="sxs-lookup"><span data-stu-id="71965-112">EXAMPLES</span></span>

### <span data-ttu-id="71965-113">Példa 1: adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="71965-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="71965-114">Ez a parancs létrehoz egy WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport WestUS helyéről.</span><span class="sxs-lookup"><span data-stu-id="71965-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="71965-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71965-115">PARAMETERS</span></span>

### <span data-ttu-id="71965-116">-Force</span><span class="sxs-lookup"><span data-stu-id="71965-116">-Force</span></span>
<span data-ttu-id="71965-117">Azt jelzi, hogy ez a parancsmag egy meglévő adattárolót cserél, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71965-117">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="71965-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="71965-118">-Location</span></span>
<span data-ttu-id="71965-119">Az adatfeldolgozó helyét adja meg, például WestUS vagy EastUS.</span><span class="sxs-lookup"><span data-stu-id="71965-119">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="71965-120">Jelenleg csak a WestUS támogatott.</span><span class="sxs-lookup"><span data-stu-id="71965-120">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="71965-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71965-121">-Name</span></span>
<span data-ttu-id="71965-122">A létrehozandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71965-122">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="71965-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71965-123">-ResourceGroupName</span></span>
<span data-ttu-id="71965-124">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71965-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="71965-125">Ez a parancsmag olyan adattípust hoz létre, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="71965-125">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="71965-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="71965-126">-Tags</span></span>
<span data-ttu-id="71965-127">Az adatfeldolgozó címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="71965-127">Specifies tags for the data factory.</span></span>

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

### <span data-ttu-id="71965-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71965-128">-Confirm</span></span>
<span data-ttu-id="71965-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71965-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71965-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71965-130">-WhatIf</span></span>
<span data-ttu-id="71965-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71965-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71965-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71965-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71965-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71965-133">-DefaultProfile</span></span>
<span data-ttu-id="71965-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71965-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71965-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71965-135">CommonParameters</span></span>
<span data-ttu-id="71965-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71965-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71965-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71965-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71965-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71965-138">INPUTS</span></span>

## <span data-ttu-id="71965-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71965-139">OUTPUTS</span></span>

### <span data-ttu-id="71965-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="71965-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="71965-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71965-141">NOTES</span></span>
* <span data-ttu-id="71965-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="71965-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="71965-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71965-143">RELATED LINKS</span></span>

[<span data-ttu-id="71965-144">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="71965-144">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="71965-145">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="71965-145">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


