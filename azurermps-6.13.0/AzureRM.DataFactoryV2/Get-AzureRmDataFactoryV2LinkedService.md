---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 8068a560954d94a134205d5e67eab19e641bed74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499627"
---
# <span data-ttu-id="f4e0a-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f4e0a-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="f4e0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e0a-103">Információt kap az adatfeldolgozó kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4e0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4e0a-104">SYNTAX</span></span>

### <span data-ttu-id="f4e0a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4e0a-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e0a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f4e0a-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e0a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4e0a-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4e0a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4e0a-108">DESCRIPTION</span></span>
<span data-ttu-id="f4e0a-109">A Get-AzureRmDataFactoryV2LinkedService parancsmag információkat kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-109">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="f4e0a-110">Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="f4e0a-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatok gyári összes kapcsolt szolgáltatásáról.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="f4e0a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f4e0a-112">EXAMPLES</span></span>

### <span data-ttu-id="f4e0a-113">1. példa: információk kérése az összes kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="f4e0a-113">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="f4e0a-114">Ez a parancs a WikiADF nevű adatfeldolgozóban található összes kapcsolt szolgáltatásról információt kap, majd a csővezeték-kezelő segítségével átadja a kapcsolt szolgáltatásokat az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f4e0a-115">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f4e0a-116">További információt a Get-Help formázása – lista című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="f4e0a-117">Az alábbi lehetőségek közül választhat:</span><span class="sxs-lookup"><span data-stu-id="f4e0a-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="f4e0a-118">2. példa: információk kérése egy adott kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="f4e0a-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="f4e0a-119">Ez a parancs információt kap a LinkedServiceCuratedWikiData nevű kapcsolt szolgáltatásról az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="f4e0a-120">3. példa: információk beszerzése egy adott kapcsolt szolgáltatásról a DataFactory paraméter megadásával</span><span class="sxs-lookup"><span data-stu-id="f4e0a-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="f4e0a-121">Az első parancs az Get-AzureRmDataFactoryV2 parancsmagot használja az ContosoFactory nevű adatfeldolgozó beolvasásához, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-121">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="f4e0a-122">A második parancs információt kap az $DataFactory-on tárolt adatfeldolgozóhoz kapcsolt szolgáltatásról, majd ezeket az információkat átadja a Format-Table parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f4e0a-123">A Format-Table parancsmag a kimenetet adatkészletként formázza a megadott tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="f4e0a-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4e0a-124">PARAMETERS</span></span>

### <span data-ttu-id="f4e0a-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4e0a-125">-DataFactory</span></span>
<span data-ttu-id="f4e0a-126">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="f4e0a-127">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4e0a-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f4e0a-128">-DataFactoryName</span></span>
<span data-ttu-id="f4e0a-129">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f4e0a-130">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4e0a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e0a-131">-DefaultProfile</span></span>
<span data-ttu-id="f4e0a-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e0a-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4e0a-133">-Name</span></span>
<span data-ttu-id="f4e0a-134">Annak a kapcsolt szolgáltatásnak a neve, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="f4e0a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e0a-135">-ResourceGroupName</span></span>
<span data-ttu-id="f4e0a-136">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f4e0a-137">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4e0a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4e0a-138">-ResourceId</span></span>
<span data-ttu-id="f4e0a-139">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f4e0a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e0a-140">CommonParameters</span></span>
<span data-ttu-id="f4e0a-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4e0a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e0a-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e0a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e0a-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4e0a-143">INPUTS</span></span>

### <span data-ttu-id="f4e0a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e0a-144">System.String</span></span>

### <span data-ttu-id="f4e0a-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f4e0a-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="f4e0a-146">Paraméterek: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4e0a-146">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="f4e0a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4e0a-147">OUTPUTS</span></span>

### <span data-ttu-id="f4e0a-148">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f4e0a-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="f4e0a-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4e0a-149">NOTES</span></span>
<span data-ttu-id="f4e0a-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="f4e0a-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f4e0a-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4e0a-151">RELATED LINKS</span></span>

[<span data-ttu-id="f4e0a-152">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f4e0a-152">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="f4e0a-153">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f4e0a-153">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
