---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8ee5ba855e1c9f9815e9dbcb844ebb23d7118d3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493555"
---
# <span data-ttu-id="5ea6a-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5ea6a-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="5ea6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ea6a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea6a-103">Információt kap az adatfeldolgozó kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ea6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ea6a-104">SYNTAX</span></span>

### <span data-ttu-id="5ea6a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ea6a-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ea6a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5ea6a-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ea6a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ea6a-107">DESCRIPTION</span></span>
<span data-ttu-id="5ea6a-108">A Get-AzureRmDataFactoryV2LinkedService parancsmag információkat kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="5ea6a-109">Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="5ea6a-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatok gyári összes kapcsolt szolgáltatásáról.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="5ea6a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5ea6a-111">EXAMPLES</span></span>

### <span data-ttu-id="5ea6a-112">1. példa: információk kérése az összes kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="5ea6a-112">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="5ea6a-113">Ez a parancs a WikiADF nevű adatfeldolgozóban található összes kapcsolt szolgáltatásról információt kap, majd a csővezeték-kezelő segítségével átadja a kapcsolt szolgáltatásokat az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5ea6a-114">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="5ea6a-115">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="5ea6a-116">Az alábbi lehetőségek közül választhat:</span><span class="sxs-lookup"><span data-stu-id="5ea6a-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="5ea6a-117">2. példa: információk kérése egy adott kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="5ea6a-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="5ea6a-118">Ez a parancs információt kap a LinkedServiceCuratedWikiData nevű kapcsolt szolgáltatásról az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="5ea6a-119">3. példa: információk beszerzése egy adott kapcsolt szolgáltatásról a DataFactory paraméter megadásával</span><span class="sxs-lookup"><span data-stu-id="5ea6a-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="5ea6a-120">Az első parancs az Get-AzureRmDataFactoryV2 parancsmagot használja az ContosoFactory nevű adatfeldolgozó beolvasásához, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="5ea6a-121">A második parancs információt kap az $DataFactory-on tárolt adatfeldolgozóhoz kapcsolt szolgáltatásról, majd ezeket az információkat átadja a Format-Table parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5ea6a-122">A Format-Table parancsmag a kimenetet adatkészletként formázza a megadott tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="5ea6a-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ea6a-123">PARAMETERS</span></span>

### <span data-ttu-id="5ea6a-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5ea6a-124">-DataFactory</span></span>
<span data-ttu-id="5ea6a-125">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="5ea6a-126">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea6a-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5ea6a-127">-DataFactoryName</span></span>
<span data-ttu-id="5ea6a-128">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5ea6a-129">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ea6a-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ea6a-130">-Name</span></span>
<span data-ttu-id="5ea6a-131">Annak a kapcsolt szolgáltatásnak a neve, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea6a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea6a-132">-ResourceGroupName</span></span>
<span data-ttu-id="5ea6a-133">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5ea6a-134">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ea6a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea6a-135">-DefaultProfile</span></span>
<span data-ttu-id="5ea6a-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ea6a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ea6a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea6a-137">CommonParameters</span></span>
<span data-ttu-id="5ea6a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ea6a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea6a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea6a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea6a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ea6a-140">INPUTS</span></span>

### <span data-ttu-id="5ea6a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5ea6a-141">System.String</span></span>
<span data-ttu-id="5ea6a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ea6a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5ea6a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ea6a-143">OUTPUTS</span></span>

### <span data-ttu-id="5ea6a-144">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ea6a-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5ea6a-145">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="5ea6a-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="5ea6a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ea6a-146">NOTES</span></span>
<span data-ttu-id="5ea6a-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="5ea6a-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5ea6a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ea6a-148">RELATED LINKS</span></span>

[<span data-ttu-id="5ea6a-149">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5ea6a-149">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="5ea6a-150">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5ea6a-150">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
