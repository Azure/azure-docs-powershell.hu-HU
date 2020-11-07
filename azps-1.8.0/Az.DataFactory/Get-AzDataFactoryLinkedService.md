---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: a54cdb0a30d0249ccb8fd177646e218e0fe604c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836545"
---
# <span data-ttu-id="2ec27-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="2ec27-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="2ec27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ec27-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec27-103">Információt kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="2ec27-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="2ec27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ec27-104">SYNTAX</span></span>

### <span data-ttu-id="2ec27-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ec27-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ec27-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2ec27-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ec27-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ec27-107">DESCRIPTION</span></span>
<span data-ttu-id="2ec27-108">A **Get-AzDataFactoryLinkedService** parancsmag információkat kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="2ec27-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="2ec27-109">Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="2ec27-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="2ec27-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatok gyári összes kapcsolt szolgáltatásáról.</span><span class="sxs-lookup"><span data-stu-id="2ec27-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="2ec27-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2ec27-111">EXAMPLES</span></span>

### <span data-ttu-id="2ec27-112">1. példa: információk kérése az összes kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="2ec27-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="2ec27-113">Ez a parancs a WikiADF nevű adatfeldolgozóban található összes kapcsolt szolgáltatásról információt kap, majd a csővezeték-kezelő segítségével átadja a kapcsolt szolgáltatásokat az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="2ec27-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ec27-114">Az adott parancsmag formázza az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="2ec27-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="2ec27-115">További információért írja be a következőt: `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="2ec27-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="2ec27-116">2. példa: információk kérése egy adott kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="2ec27-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="2ec27-117">Ez a parancs információt kap a HDILinkedService nevű kapcsolt szolgáltatásról az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="2ec27-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="2ec27-118">3. példa: információk beszerzése egy adott kapcsolt szolgáltatásról a DataFactory paraméter megadásával</span><span class="sxs-lookup"><span data-stu-id="2ec27-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="2ec27-119">Az első parancs az Get-AzDataFactory parancsmagot használja az ContosoFactory nevű adatfeldolgozó beolvasásához, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2ec27-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="2ec27-120">A második parancs információt kap az $DataFactory-on tárolt adatfeldolgozóhoz kapcsolt szolgáltatásról, majd ezeket az információkat átadja a Format-Table parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="2ec27-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ec27-121">**Formátum – a táblázat** a kimenetet adatkészletként formázza, és a megadott tulajdonságokat adatkészlet-oszlopként adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ec27-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="2ec27-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ec27-122">PARAMETERS</span></span>

### <span data-ttu-id="2ec27-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2ec27-123">-DataFactory</span></span>
<span data-ttu-id="2ec27-124">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2ec27-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2ec27-125">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ec27-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ec27-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2ec27-126">-DataFactoryName</span></span>
<span data-ttu-id="2ec27-127">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ec27-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2ec27-128">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ec27-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ec27-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec27-129">-DefaultProfile</span></span>
<span data-ttu-id="2ec27-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2ec27-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ec27-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ec27-131">-Name</span></span>
<span data-ttu-id="2ec27-132">Annak a kapcsolt szolgáltatásnak a neve, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="2ec27-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="2ec27-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec27-133">-ResourceGroupName</span></span>
<span data-ttu-id="2ec27-134">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ec27-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2ec27-135">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="2ec27-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ec27-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec27-136">CommonParameters</span></span>
<span data-ttu-id="2ec27-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ec27-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec27-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec27-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec27-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ec27-139">INPUTS</span></span>

### <span data-ttu-id="2ec27-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2ec27-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="2ec27-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec27-141">System.String</span></span>

## <span data-ttu-id="2ec27-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ec27-142">OUTPUTS</span></span>

### <span data-ttu-id="2ec27-143">Microsoft. Azure. Command. DataFactories. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="2ec27-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="2ec27-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ec27-144">NOTES</span></span>
* <span data-ttu-id="2ec27-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="2ec27-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2ec27-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ec27-146">RELATED LINKS</span></span>

[<span data-ttu-id="2ec27-147">Új – AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="2ec27-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="2ec27-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="2ec27-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


