---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182532"
---
# <span data-ttu-id="be36e-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="be36e-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="be36e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be36e-102">SYNOPSIS</span></span>
<span data-ttu-id="be36e-103">Információt kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="be36e-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="be36e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be36e-104">SYNTAX</span></span>

### <span data-ttu-id="be36e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be36e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be36e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="be36e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be36e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="be36e-107">DESCRIPTION</span></span>
<span data-ttu-id="be36e-108">A **Get-AzDataFactoryHub** parancsmag információkat kap az Azure Data Factory hubokról.</span><span class="sxs-lookup"><span data-stu-id="be36e-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="be36e-109">Ha a hub nevét adja meg, ez a parancsmag információkat kap a hub-ról.</span><span class="sxs-lookup"><span data-stu-id="be36e-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="be36e-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatgyárban található összes hubokról.</span><span class="sxs-lookup"><span data-stu-id="be36e-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="be36e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="be36e-111">EXAMPLES</span></span>

### <span data-ttu-id="be36e-112">Példa 1: az összes adathub beolvasása</span><span class="sxs-lookup"><span data-stu-id="be36e-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="be36e-113">Ez a parancs minden adatközpontot beolvas a ADFResourceGroup nevű Azure Resource nevű csoportba, és az ADFDataFactory nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="be36e-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="be36e-114">2. példa: adott adatközpont beszerzése</span><span class="sxs-lookup"><span data-stu-id="be36e-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="be36e-115">Ez a parancs információt kap a MyDataHub nevű hub-ról a ADFResourceGroup nevű Azure Resource csoportban, valamint az ADFDataFactory nevű adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="be36e-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="be36e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be36e-116">PARAMETERS</span></span>

### <span data-ttu-id="be36e-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="be36e-117">-DataFactory</span></span>
<span data-ttu-id="be36e-118">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="be36e-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="be36e-119">Ez a parancsmag információt ad az adatfeldolgozó hubokról, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="be36e-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="be36e-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="be36e-120">-DataFactoryName</span></span>
<span data-ttu-id="be36e-121">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be36e-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="be36e-122">Ez a parancsmag információt ad az adatfeldolgozó hubokról, amelyeket ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="be36e-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="be36e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be36e-123">-DefaultProfile</span></span>
<span data-ttu-id="be36e-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="be36e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be36e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be36e-125">-Name</span></span>
<span data-ttu-id="be36e-126">Annak a hub-nak a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="be36e-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="be36e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be36e-127">-ResourceGroupName</span></span>
<span data-ttu-id="be36e-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be36e-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="be36e-129">Ez a parancsmag a paraméter által megadott csoportba tartozó hubokról ad információkat.</span><span class="sxs-lookup"><span data-stu-id="be36e-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="be36e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be36e-130">CommonParameters</span></span>
<span data-ttu-id="be36e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be36e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be36e-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be36e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be36e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be36e-133">INPUTS</span></span>

### <span data-ttu-id="be36e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="be36e-134">System.String</span></span>

### <span data-ttu-id="be36e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="be36e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="be36e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be36e-136">OUTPUTS</span></span>

### <span data-ttu-id="be36e-137">Microsoft. Azure. Command. DataFactories. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="be36e-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="be36e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be36e-138">NOTES</span></span>
* <span data-ttu-id="be36e-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="be36e-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="be36e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be36e-140">RELATED LINKS</span></span>

[<span data-ttu-id="be36e-141">Új – AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="be36e-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="be36e-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="be36e-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


