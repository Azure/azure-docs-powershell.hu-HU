---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847226"
---
# <span data-ttu-id="ea7ca-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ea7ca-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="ea7ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7ca-103">Az Azure Data Factory hub-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="ea7ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea7ca-104">SYNTAX</span></span>

### <span data-ttu-id="ea7ca-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea7ca-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea7ca-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ea7ca-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea7ca-107">DESCRIPTION</span></span>
<span data-ttu-id="ea7ca-108">A **New-AzDataFactoryHub** parancsmag létrehoz egy hubot az Azure Data Factory számára a megadott Azure-erőforrás csoportban és a megadott fájlformátumban.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="ea7ca-109">Miután létrehozta a hubot, használhatja a kapcsolt szolgáltatások tárolását és kezelését a csoportban, és felveheti a csővezetékeket a középpontba.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="ea7ca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ea7ca-110">EXAMPLES</span></span>

### <span data-ttu-id="ea7ca-111">Példa 1: hub létrehozása</span><span class="sxs-lookup"><span data-stu-id="ea7ca-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="ea7ca-112">Ez a parancs létrehoz egy ContosoDataHub nevű hubot az erőforráscsoport ADFResourceGroup és az ADFDataFactory nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="ea7ca-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea7ca-113">PARAMETERS</span></span>

### <span data-ttu-id="ea7ca-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ea7ca-114">-DataFactory</span></span>
<span data-ttu-id="ea7ca-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ea7ca-116">Ez a parancsmag létrehoz egy hubot az adatfeldolgozó számára, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea7ca-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ea7ca-117">-DataFactoryName</span></span>
<span data-ttu-id="ea7ca-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ea7ca-119">Ez a parancsmag létrehoz egy hubot az adatfeldolgozó számára, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea7ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7ca-120">-DefaultProfile</span></span>
<span data-ttu-id="ea7ca-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ea7ca-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea7ca-122">-Fájl</span><span class="sxs-lookup"><span data-stu-id="ea7ca-122">-File</span></span>
<span data-ttu-id="ea7ca-123">Annak a JavaScript-objektumnak a teljes elérési útját adja meg, amely a hub leírását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7ca-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ea7ca-124">-Force</span></span>
<span data-ttu-id="ea7ca-125">Azt jelzi, hogy ez a parancsmag egy meglévő hubot cserél le anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ea7ca-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea7ca-126">-Name</span></span>
<span data-ttu-id="ea7ca-127">A létrehozandó hub nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="ea7ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea7ca-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ea7ca-130">Ez a parancsmag létrehoz egy olyan hubot, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea7ca-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea7ca-131">-Confirm</span></span>
<span data-ttu-id="ea7ca-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7ca-133">-WhatIf</span></span>
<span data-ttu-id="ea7ca-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7ca-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7ca-136">CommonParameters</span></span>
<span data-ttu-id="ea7ca-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea7ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7ca-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7ca-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7ca-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea7ca-139">INPUTS</span></span>

### <span data-ttu-id="ea7ca-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ea7ca-140">System.String</span></span>

### <span data-ttu-id="ea7ca-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ea7ca-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ea7ca-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea7ca-142">OUTPUTS</span></span>

### <span data-ttu-id="ea7ca-143">Microsoft. Azure. Command. DataFactories. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="ea7ca-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="ea7ca-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea7ca-144">NOTES</span></span>
* <span data-ttu-id="ea7ca-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="ea7ca-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ea7ca-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea7ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="ea7ca-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ea7ca-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="ea7ca-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ea7ca-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


