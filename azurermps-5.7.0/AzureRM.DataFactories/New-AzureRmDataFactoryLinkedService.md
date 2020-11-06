---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: c89a7950b70bf3b3b13b053e4e007434afdb078d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496620"
---
# <span data-ttu-id="b9b64-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b9b64-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="b9b64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9b64-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b64-103">Az adattárolók vagy a Felhőbeli szolgáltatások kapcsolata az Azure Data Factory szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="b9b64-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9b64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9b64-104">SYNTAX</span></span>

### <span data-ttu-id="b9b64-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9b64-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9b64-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b9b64-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b64-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9b64-107">DESCRIPTION</span></span>
<span data-ttu-id="b9b64-108">A **New-AzureRmDataFactoryLinkedService** parancsmag egy adattárral vagy egy felhőalapú szolgáltatással kapcsolódik az Azure Data Factory szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="b9b64-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="b9b64-109">Ha már létezik egy olyan kapcsolt szolgáltatás neve, amely már létezik, ez a parancsmag a kapcsolt szolgáltatás cseréje előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9b64-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="b9b64-110">Ha az *erő* paramétert adja meg, a parancsmag megerősítés nélkül felülírja a meglévő kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b9b64-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="b9b64-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="b9b64-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="b9b64-112">Adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9b64-112">Create a data factory.</span></span> 
- <span data-ttu-id="b9b64-113">Kapcsolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9b64-113">Create linked services.</span></span> 
- <span data-ttu-id="b9b64-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9b64-114">Create datasets.</span></span> 
- <span data-ttu-id="b9b64-115">Csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9b64-115">Create a pipeline.</span></span>

## <span data-ttu-id="b9b64-116">Példák</span><span class="sxs-lookup"><span data-stu-id="b9b64-116">EXAMPLES</span></span>

### <span data-ttu-id="b9b64-117">1. példa: kapcsolt szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9b64-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="b9b64-118">Ez a parancs létrehoz egy LinkedServiceCuratedWikiData nevű hivatkozást a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="b9b64-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="b9b64-119">Ez a hivatkozás egy, a fájlban megadott Azure Blob-tárolóhoz csatolja a WikiADF nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="b9b64-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="b9b64-120">A parancs a csővezeték-kezelő használatával átadja az eredményt az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b9b64-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b9b64-121">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="b9b64-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="b9b64-122">További információért írja be a következőt: `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="b9b64-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="b9b64-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9b64-123">PARAMETERS</span></span>

### <span data-ttu-id="b9b64-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b9b64-124">-DataFactory</span></span>
<span data-ttu-id="b9b64-125">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b9b64-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b9b64-126">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást az adatgyárhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9b64-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9b64-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b9b64-127">-DataFactoryName</span></span>
<span data-ttu-id="b9b64-128">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9b64-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b9b64-129">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást az adatgyárhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9b64-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9b64-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b64-130">-DefaultProfile</span></span>
<span data-ttu-id="b9b64-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9b64-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9b64-132">-Fájl</span><span class="sxs-lookup"><span data-stu-id="b9b64-132">-File</span></span>
<span data-ttu-id="b9b64-133">Annak a JavaScript-objektumnak a teljes elérési útját adja meg, amely a kapcsolt szolgáltatás leírását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b9b64-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b64-134">-Force</span><span class="sxs-lookup"><span data-stu-id="b9b64-134">-Force</span></span>
<span data-ttu-id="b9b64-135">Azt jelzi, hogy ez a parancsmag egy meglévő kapcsolt szolgáltatás lecserélése nélkül kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9b64-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b64-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9b64-136">-Name</span></span>
<span data-ttu-id="b9b64-137">A létrehozandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9b64-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="b9b64-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b64-138">-ResourceGroupName</span></span>
<span data-ttu-id="b9b64-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9b64-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b9b64-140">Ez a parancsmag létrehoz egy olyan kapcsolt szolgáltatást a csoporthoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="b9b64-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9b64-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9b64-141">-Confirm</span></span>
<span data-ttu-id="b9b64-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9b64-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b64-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b64-143">-WhatIf</span></span>
<span data-ttu-id="b9b64-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9b64-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b64-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9b64-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b64-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b64-146">CommonParameters</span></span>
<span data-ttu-id="b9b64-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9b64-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b64-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b64-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b64-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9b64-149">INPUTS</span></span>

### <span data-ttu-id="b9b64-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="b9b64-150">None</span></span>
<span data-ttu-id="b9b64-151">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b9b64-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9b64-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9b64-152">OUTPUTS</span></span>

### <span data-ttu-id="b9b64-153">Microsoft. WindowsAzure. Command. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b9b64-153">Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="b9b64-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9b64-154">NOTES</span></span>
* <span data-ttu-id="b9b64-155">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="b9b64-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b9b64-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9b64-156">RELATED LINKS</span></span>

[<span data-ttu-id="b9b64-157">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b9b64-157">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="b9b64-158">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b9b64-158">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


