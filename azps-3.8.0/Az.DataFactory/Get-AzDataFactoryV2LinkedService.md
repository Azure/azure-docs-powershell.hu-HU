---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847273"
---
# <span data-ttu-id="7efd9-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="7efd9-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="7efd9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7efd9-102">SYNOPSIS</span></span>
<span data-ttu-id="7efd9-103">Információt kap az adatfeldolgozó kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="7efd9-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="7efd9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7efd9-104">SYNTAX</span></span>

### <span data-ttu-id="7efd9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7efd9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7efd9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7efd9-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7efd9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7efd9-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7efd9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7efd9-108">DESCRIPTION</span></span>
<span data-ttu-id="7efd9-109">A Get-AzDataFactoryV2LinkedService parancsmag információkat kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="7efd9-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="7efd9-110">Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="7efd9-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="7efd9-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatok gyári összes kapcsolt szolgáltatásáról.</span><span class="sxs-lookup"><span data-stu-id="7efd9-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="7efd9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7efd9-112">EXAMPLES</span></span>

### <span data-ttu-id="7efd9-113">1. példa: információk kérése az összes kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="7efd9-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

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

<span data-ttu-id="7efd9-114">Ez a parancs a WikiADF nevű adatfeldolgozóban található összes kapcsolt szolgáltatásról információt kap, majd a csővezeték-kezelő segítségével átadja a kapcsolt szolgáltatásokat az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="7efd9-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7efd9-115">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="7efd9-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="7efd9-116">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="7efd9-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="7efd9-117">Az alábbi lehetőségek közül választhat:</span><span class="sxs-lookup"><span data-stu-id="7efd9-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="7efd9-118">2. példa: információk kérése egy adott kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="7efd9-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="7efd9-119">Ez a parancs információt kap a LinkedServiceCuratedWikiData nevű kapcsolt szolgáltatásról az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="7efd9-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="7efd9-120">3. példa: információk beszerzése egy adott kapcsolt szolgáltatásról a DataFactory paraméter megadásával</span><span class="sxs-lookup"><span data-stu-id="7efd9-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="7efd9-121">Az első parancs az Get-AzDataFactoryV2 parancsmagot használja az ContosoFactory nevű adatfeldolgozó beolvasásához, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7efd9-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="7efd9-122">A második parancs információt kap az $DataFactory-on tárolt adatfeldolgozóhoz kapcsolt szolgáltatásról, majd ezeket az információkat átadja a Format-Table parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="7efd9-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7efd9-123">A Format-Table parancsmag a kimenetet adatkészletként formázza a megadott tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="7efd9-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="7efd9-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7efd9-124">PARAMETERS</span></span>

### <span data-ttu-id="7efd9-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7efd9-125">-DataFactory</span></span>
<span data-ttu-id="7efd9-126">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7efd9-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="7efd9-127">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7efd9-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7efd9-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7efd9-128">-DataFactoryName</span></span>
<span data-ttu-id="7efd9-129">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7efd9-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7efd9-130">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7efd9-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7efd9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efd9-131">-DefaultProfile</span></span>
<span data-ttu-id="7efd9-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7efd9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7efd9-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7efd9-133">-Name</span></span>
<span data-ttu-id="7efd9-134">Annak a kapcsolt szolgáltatásnak a neve, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="7efd9-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efd9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efd9-135">-ResourceGroupName</span></span>
<span data-ttu-id="7efd9-136">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7efd9-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7efd9-137">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="7efd9-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7efd9-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7efd9-138">-ResourceId</span></span>
<span data-ttu-id="7efd9-139">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="7efd9-139">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efd9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efd9-140">CommonParameters</span></span>
<span data-ttu-id="7efd9-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7efd9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efd9-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efd9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efd9-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7efd9-143">INPUTS</span></span>

### <span data-ttu-id="7efd9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7efd9-144">System.String</span></span>

### <span data-ttu-id="7efd9-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7efd9-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7efd9-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7efd9-146">OUTPUTS</span></span>

### <span data-ttu-id="7efd9-147">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="7efd9-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="7efd9-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7efd9-148">NOTES</span></span>
<span data-ttu-id="7efd9-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="7efd9-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7efd9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7efd9-150">RELATED LINKS</span></span>

[<span data-ttu-id="7efd9-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="7efd9-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="7efd9-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="7efd9-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
