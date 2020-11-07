---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: cca0b397f85a0e0fd42f1e3331294881e1e89014
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672025"
---
# <span data-ttu-id="0ce03-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0ce03-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="0ce03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ce03-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce03-103">Információt kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="0ce03-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ce03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ce03-104">SYNTAX</span></span>

### <span data-ttu-id="0ce03-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ce03-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ce03-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0ce03-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ce03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ce03-107">DESCRIPTION</span></span>
<span data-ttu-id="0ce03-108">A **Get-AzureRmDataFactoryHub** parancsmag információkat kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="0ce03-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="0ce03-109">Ha a hub nevét adja meg, ez a parancsmag információkat kap a hub-ról.</span><span class="sxs-lookup"><span data-stu-id="0ce03-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="0ce03-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes hubokról.</span><span class="sxs-lookup"><span data-stu-id="0ce03-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="0ce03-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0ce03-111">EXAMPLES</span></span>

### <span data-ttu-id="0ce03-112">Példa 1: az összes adathub beolvasása</span><span class="sxs-lookup"><span data-stu-id="0ce03-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="0ce03-113">Ez a parancs minden adatközpontot beolvas a ADFResourceGroup nevű Azure Resource nevű csoportba, és az ADFDataFactory nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="0ce03-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="0ce03-114">2. példa: adott adatközpont beszerzése</span><span class="sxs-lookup"><span data-stu-id="0ce03-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="0ce03-115">Ez a parancs információt kap a MyDataHub nevű hub-ról a ADFResourceGroup nevű Azure Resource csoportban, valamint az ADFDataFactory nevű adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="0ce03-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="0ce03-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ce03-116">PARAMETERS</span></span>

### <span data-ttu-id="0ce03-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0ce03-117">-DataFactory</span></span>
<span data-ttu-id="0ce03-118">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0ce03-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0ce03-119">Ez a parancsmag információt ad az adatfeldolgozó hubokról, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="0ce03-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce03-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0ce03-120">-DataFactoryName</span></span>
<span data-ttu-id="0ce03-121">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ce03-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0ce03-122">Ez a parancsmag információt ad az adatfeldolgozó hubokról, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="0ce03-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce03-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce03-123">-DefaultProfile</span></span>
<span data-ttu-id="0ce03-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ce03-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ce03-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ce03-125">-Name</span></span>
<span data-ttu-id="0ce03-126">Annak a hub-nak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="0ce03-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce03-127">-ResourceGroupName</span></span>
<span data-ttu-id="0ce03-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ce03-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0ce03-129">Ez a parancsmag a paraméter által megadott csoportba tartozó hubokról ad információkat.</span><span class="sxs-lookup"><span data-stu-id="0ce03-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce03-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce03-130">CommonParameters</span></span>
<span data-ttu-id="0ce03-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ce03-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce03-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce03-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce03-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ce03-133">INPUTS</span></span>

### <span data-ttu-id="0ce03-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ce03-134">None</span></span>
<span data-ttu-id="0ce03-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0ce03-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ce03-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ce03-136">OUTPUTS</span></span>

### <span data-ttu-id="0ce03-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. DataFactories. models. PSHub]</span><span class="sxs-lookup"><span data-stu-id="0ce03-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="0ce03-138">Microsoft. Azure. Command. DataFactories. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="0ce03-138">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="0ce03-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ce03-139">NOTES</span></span>
* <span data-ttu-id="0ce03-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="0ce03-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0ce03-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ce03-141">RELATED LINKS</span></span>

[<span data-ttu-id="0ce03-142">Új – AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0ce03-142">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="0ce03-143">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0ce03-143">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


