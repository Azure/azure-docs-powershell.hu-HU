---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 0312b3d2a5ffa973c4ef2934ea592844850d8018
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930194"
---
# <span data-ttu-id="bfec3-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="bfec3-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="bfec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfec3-102">SYNOPSIS</span></span>
<span data-ttu-id="bfec3-103">Információkat kap a Data Factory csatolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="bfec3-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="bfec3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfec3-104">SYNTAX</span></span>

### <span data-ttu-id="bfec3-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfec3-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfec3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bfec3-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfec3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfec3-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfec3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfec3-108">DESCRIPTION</span></span>
<span data-ttu-id="bfec3-109">A Get-AzDataFactoryV2LinkedService parancsmag információkat kap az Azure Data Factory csatolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="bfec3-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="bfec3-110">Ha megadja egy csatolt szolgáltatás nevét, ez a parancsmag információt kap a hivatkozott szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="bfec3-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="bfec3-111">Ha nem ad meg nevet, ez a parancsmag információt kap az adatüzemben található összes csatolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="bfec3-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="bfec3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfec3-112">EXAMPLES</span></span>

### <span data-ttu-id="bfec3-113">1. példa: Információk az összes csatolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="bfec3-113">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="bfec3-114">Ez a parancs információkat kap a WikiADF nevű adatüzemeltetőben található összes csatolt szolgáltatásról, majd a folyamat műveleti Format-List segítségével átadja a csatolt szolgáltatásokat a Format-List-parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfec3-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bfec3-115">Ez a Windows PowerShell-parancsmag formázta az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="bfec3-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="bfec3-116">További információért írja be a Get-Help formátumlistát.</span><span class="sxs-lookup"><span data-stu-id="bfec3-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="bfec3-117">Az alábbi módszerek közül választhat:</span><span class="sxs-lookup"><span data-stu-id="bfec3-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="bfec3-118">2. példa: Információk lekérte egy adott csatolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="bfec3-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="bfec3-119">Ez a parancs információkat kap a LinkedServiceCuratedWikiData nevű csatolt szolgáltatásról a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="bfec3-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="bfec3-120">3. példa: Információ lekérte egy adott csatolt szolgáltatásról a DataFactory paraméter megadásával</span><span class="sxs-lookup"><span data-stu-id="bfec3-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="bfec3-121">Az első parancs a Get-AzDataFactoryV2 parancsmag használatával begyűjte a ContosoFactory nevű adat factoryt, majd tárolja azt a $DataFactory változóban.</span><span class="sxs-lookup"><span data-stu-id="bfec3-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="bfec3-122">A második parancs információkat kap a $DataFactory-ban tárolt adatüzemeltető csatolt szolgáltatásról, majd Format-Table folyamatkezelő parancsmag használatával átadja az adatokat a Format-Table-parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="bfec3-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bfec3-123">A Format-Table parancsmag a kimenetet adatkészletként formázja a megadott tulajdonságokkal adatkészletoszlopokként.</span><span class="sxs-lookup"><span data-stu-id="bfec3-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="bfec3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfec3-124">PARAMETERS</span></span>

### <span data-ttu-id="bfec3-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bfec3-125">-DataFactory</span></span>
<span data-ttu-id="bfec3-126">EGY PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bfec3-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="bfec3-127">Ez a parancsmag olyan csatolt szolgáltatásokat kap, amelyek a paraméter által megadott adatüzemhez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="bfec3-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfec3-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bfec3-128">-DataFactoryName</span></span>
<span data-ttu-id="bfec3-129">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfec3-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bfec3-130">Ez a parancsmag olyan csatolt szolgáltatásokat kap, amelyek a paraméter által megadott adatüzemhez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="bfec3-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfec3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfec3-131">-DefaultProfile</span></span>
<span data-ttu-id="bfec3-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfec3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfec3-133">-Name</span><span class="sxs-lookup"><span data-stu-id="bfec3-133">-Name</span></span>
<span data-ttu-id="bfec3-134">Annak a csatolt szolgáltatásnak a nevét adja meg, amelyről információt kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="bfec3-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="bfec3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfec3-135">-ResourceGroupName</span></span>
<span data-ttu-id="bfec3-136">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfec3-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bfec3-137">Ez a parancsmag olyan csatolt szolgáltatásokat kap, amelyek a paraméter által megadott csoporthoz tartoznak.</span><span class="sxs-lookup"><span data-stu-id="bfec3-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bfec3-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfec3-138">-ResourceId</span></span>
<span data-ttu-id="bfec3-139">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="bfec3-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bfec3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfec3-140">CommonParameters</span></span>
<span data-ttu-id="bfec3-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfec3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfec3-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfec3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfec3-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfec3-143">INPUTS</span></span>

### <span data-ttu-id="bfec3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bfec3-144">System.String</span></span>

### <span data-ttu-id="bfec3-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bfec3-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bfec3-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfec3-146">OUTPUTS</span></span>

### <span data-ttu-id="bfec3-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="bfec3-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="bfec3-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfec3-148">NOTES</span></span>
<span data-ttu-id="bfec3-149">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="bfec3-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bfec3-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfec3-150">RELATED LINKS</span></span>

[<span data-ttu-id="bfec3-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="bfec3-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="bfec3-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="bfec3-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
