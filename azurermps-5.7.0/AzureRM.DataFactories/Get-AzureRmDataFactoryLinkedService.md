---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7034e17e119acb1077cf17dca85ded8a40cb2e2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497644"
---
# <span data-ttu-id="31e04-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="31e04-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="31e04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31e04-102">SYNOPSIS</span></span>
<span data-ttu-id="31e04-103">Információt kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="31e04-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31e04-104">SYNTAX</span></span>

### <span data-ttu-id="31e04-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31e04-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31e04-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="31e04-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e04-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="31e04-107">DESCRIPTION</span></span>
<span data-ttu-id="31e04-108">A **Get-AzureRmDataFactoryLinkedService** parancsmag információkat kap az Azure Data Factory kapcsolt szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="31e04-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="31e04-109">Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="31e04-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="31e04-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatok gyári összes kapcsolt szolgáltatásáról.</span><span class="sxs-lookup"><span data-stu-id="31e04-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="31e04-111">Példák</span><span class="sxs-lookup"><span data-stu-id="31e04-111">EXAMPLES</span></span>

### <span data-ttu-id="31e04-112">1. példa: információk kérése az összes kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="31e04-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="31e04-113">Ez a parancs a WikiADF nevű adatfeldolgozóban található összes kapcsolt szolgáltatásról információt kap, majd a csővezeték-kezelő segítségével átadja a kapcsolt szolgáltatásokat az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="31e04-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31e04-114">Az adott parancsmag formázza az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="31e04-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="31e04-115">További információért írja be a következőt: `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="31e04-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="31e04-116">2. példa: információk kérése egy adott kapcsolt szolgáltatásról</span><span class="sxs-lookup"><span data-stu-id="31e04-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="31e04-117">Ez a parancs információt kap a HDILinkedService nevű kapcsolt szolgáltatásról az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="31e04-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="31e04-118">3. példa: információk beszerzése egy adott kapcsolt szolgáltatásról a DataFactory paraméter megadásával</span><span class="sxs-lookup"><span data-stu-id="31e04-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="31e04-119">Az első parancs az Get-AzureRmDataFactory parancsmagot használja az ContosoFactory nevű adatfeldolgozó beolvasásához, majd a $DataFactory változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="31e04-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="31e04-120">A második parancs információt kap az $DataFactory-on tárolt adatfeldolgozóhoz kapcsolt szolgáltatásról, majd ezeket az információkat átadja a Format-Table parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="31e04-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31e04-121">**Formátum – a táblázat** a kimenetet adatkészletként formázza, és a megadott tulajdonságokat adatkészlet-oszlopként adja meg.</span><span class="sxs-lookup"><span data-stu-id="31e04-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="31e04-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31e04-122">PARAMETERS</span></span>

### <span data-ttu-id="31e04-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e04-123">-DataFactory</span></span>
<span data-ttu-id="31e04-124">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="31e04-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="31e04-125">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="31e04-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="31e04-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="31e04-126">-DataFactoryName</span></span>
<span data-ttu-id="31e04-127">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31e04-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="31e04-128">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek az adatgyárhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="31e04-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="31e04-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e04-129">-DefaultProfile</span></span>
<span data-ttu-id="31e04-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="31e04-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31e04-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31e04-131">-Name</span></span>
<span data-ttu-id="31e04-132">Annak a kapcsolt szolgáltatásnak a neve, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="31e04-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="31e04-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e04-133">-ResourceGroupName</span></span>
<span data-ttu-id="31e04-134">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31e04-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="31e04-135">Ez a parancsmag olyan kapcsolt szolgáltatásokat kap, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="31e04-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="31e04-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e04-136">CommonParameters</span></span>
<span data-ttu-id="31e04-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31e04-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e04-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e04-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e04-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31e04-139">INPUTS</span></span>

### <span data-ttu-id="31e04-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="31e04-140">None</span></span>
<span data-ttu-id="31e04-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="31e04-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31e04-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31e04-142">OUTPUTS</span></span>

### <span data-ttu-id="31e04-143">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. Command. Utilities. PSLinkedService, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. commands. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="31e04-143">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="31e04-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31e04-144">NOTES</span></span>
* <span data-ttu-id="31e04-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="31e04-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="31e04-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31e04-146">RELATED LINKS</span></span>

[<span data-ttu-id="31e04-147">Új – AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="31e04-147">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="31e04-148">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="31e04-148">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


