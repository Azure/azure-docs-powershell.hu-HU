---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: a96d8d3d9025e473b5c08d84201fde2a10d8be34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505123"
---
# <span data-ttu-id="7f186-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7f186-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="7f186-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f186-102">SYNOPSIS</span></span>
<span data-ttu-id="7f186-103">Információt kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="7f186-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f186-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f186-104">SYNTAX</span></span>

### <span data-ttu-id="7f186-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f186-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f186-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7f186-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f186-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f186-107">DESCRIPTION</span></span>
<span data-ttu-id="7f186-108">A **Get-AzureRmDataFactoryHub** parancsmag információkat kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="7f186-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="7f186-109">Ha a hub nevét adja meg, ez a parancsmag információkat kap a hub-ról.</span><span class="sxs-lookup"><span data-stu-id="7f186-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="7f186-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes hubokról.</span><span class="sxs-lookup"><span data-stu-id="7f186-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="7f186-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7f186-111">EXAMPLES</span></span>

### <span data-ttu-id="7f186-112">Példa 1: az összes adathub beolvasása</span><span class="sxs-lookup"><span data-stu-id="7f186-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="7f186-113">Ez a parancs minden adatközpontot beolvas a ADFResourceGroup nevű Azure Resource nevű csoportba, és az ADFDataFactory nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="7f186-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="7f186-114">2. példa: adott adatközpont beszerzése</span><span class="sxs-lookup"><span data-stu-id="7f186-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="7f186-115">Ez a parancs információt kap a MyDataHub nevű hub-ról a ADFResourceGroup nevű Azure Resource csoportban, valamint az ADFDataFactory nevű adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="7f186-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="7f186-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f186-116">PARAMETERS</span></span>

### <span data-ttu-id="7f186-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7f186-117">-DataFactory</span></span>
<span data-ttu-id="7f186-118">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7f186-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7f186-119">Ez a parancsmag információt ad az adatfeldolgozó hubokról, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7f186-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f186-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7f186-120">-DataFactoryName</span></span>
<span data-ttu-id="7f186-121">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f186-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7f186-122">Ez a parancsmag információt ad az adatfeldolgozó hubokról, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7f186-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f186-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f186-123">-Name</span></span>
<span data-ttu-id="7f186-124">Annak a hub-nak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="7f186-124">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f186-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f186-125">-ResourceGroupName</span></span>
<span data-ttu-id="7f186-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f186-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7f186-127">Ez a parancsmag a paraméter által megadott csoportba tartozó hubokról ad információkat.</span><span class="sxs-lookup"><span data-stu-id="7f186-127">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f186-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f186-128">-DefaultProfile</span></span>
<span data-ttu-id="7f186-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f186-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f186-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f186-130">CommonParameters</span></span>
<span data-ttu-id="7f186-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f186-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f186-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f186-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f186-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f186-133">INPUTS</span></span>

## <span data-ttu-id="7f186-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f186-134">OUTPUTS</span></span>

### <span data-ttu-id="7f186-135">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. DataFactories. models. PSHub]</span><span class="sxs-lookup"><span data-stu-id="7f186-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="7f186-136">Microsoft. Azure. Command. DataFactories. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="7f186-136">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="7f186-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f186-137">NOTES</span></span>
* <span data-ttu-id="7f186-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="7f186-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7f186-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f186-139">RELATED LINKS</span></span>

[<span data-ttu-id="7f186-140">Új – AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7f186-140">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="7f186-141">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7f186-141">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


