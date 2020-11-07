---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b7a608e4bed6e68f06660f10f2ef72effb6ad18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672540"
---
# <span data-ttu-id="6a2a0-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="6a2a0-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="6a2a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2a0-103">Beolvassa az adattó-statisztika-katalógus elemeit vagy típusait.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a2a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a2a0-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a2a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2a0-106">A **Get-AzureRmDataLakeAnalyticsCatalogItem** megkapja az Azure Data Lake-tó elemzési elemét, vagy egy megadott típusú katalógust kap.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="6a2a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="6a2a0-108">Példa 1: megadott adatbázis beszerzése</span><span class="sxs-lookup"><span data-stu-id="6a2a0-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="6a2a0-109">Ez a parancs a megadott adatbázist kapja.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-109">This command gets the specified database.</span></span>

### <span data-ttu-id="6a2a0-110">2. példa: táblázatok beszerzése egy megadott adatbázisban és sémában</span><span class="sxs-lookup"><span data-stu-id="6a2a0-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="6a2a0-111">Ez a parancs a megadott adatbázisban lévő táblák listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="6a2a0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a2a0-112">PARAMETERS</span></span>

### <span data-ttu-id="6a2a0-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="6a2a0-113">-Account</span></span>
<span data-ttu-id="6a2a0-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2a0-115">-DefaultProfile</span></span>
<span data-ttu-id="6a2a0-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a2a0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a2a0-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="6a2a0-117">-ItemType</span></span>
<span data-ttu-id="6a2a0-118">A beolvasott vagy a listán szereplő elem (ek) katalógus-elemének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="6a2a0-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6a2a0-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a2a0-120">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="6a2a0-120">Database</span></span>
- <span data-ttu-id="6a2a0-121">Séma</span><span class="sxs-lookup"><span data-stu-id="6a2a0-121">Schema</span></span>
- <span data-ttu-id="6a2a0-122">Összeállítási</span><span class="sxs-lookup"><span data-stu-id="6a2a0-122">Assembly</span></span>
- <span data-ttu-id="6a2a0-123">Táblázat</span><span class="sxs-lookup"><span data-stu-id="6a2a0-123">Table</span></span>
- <span data-ttu-id="6a2a0-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="6a2a0-124">TableValuedFunction</span></span>
- <span data-ttu-id="6a2a0-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="6a2a0-125">TableStatistics</span></span>
- <span data-ttu-id="6a2a0-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="6a2a0-126">ExternalDataSource</span></span>
- <span data-ttu-id="6a2a0-127">Nézd</span><span class="sxs-lookup"><span data-stu-id="6a2a0-127">View</span></span>
- <span data-ttu-id="6a2a0-128">Eljárás</span><span class="sxs-lookup"><span data-stu-id="6a2a0-128">Procedure</span></span>
- <span data-ttu-id="6a2a0-129">Titkos</span><span class="sxs-lookup"><span data-stu-id="6a2a0-129">Secret</span></span>
- <span data-ttu-id="6a2a0-130">Hitelesítőadat</span><span class="sxs-lookup"><span data-stu-id="6a2a0-130">Credential</span></span>
- <span data-ttu-id="6a2a0-131">Típusú</span><span class="sxs-lookup"><span data-stu-id="6a2a0-131">Types</span></span>
- <span data-ttu-id="6a2a0-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="6a2a0-132">TablePartition</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2a0-133">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="6a2a0-133">-Path</span></span>
<span data-ttu-id="6a2a0-134">A beolvasandó elem többrészes elérési útja vagy a lista elemeinek a fölérendelt eleme.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="6a2a0-135">Az elérési út egyes részeit ponttal (.) kell elválasztani.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2a0-136">CommonParameters</span></span>
<span data-ttu-id="6a2a0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a2a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2a0-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2a0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2a0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a2a0-139">INPUTS</span></span>

### <span data-ttu-id="6a2a0-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a2a0-140">None</span></span>
<span data-ttu-id="6a2a0-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a2a0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a2a0-142">OUTPUTS</span></span>

### <span data-ttu-id="6a2a0-143">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="6a2a0-143">CatalogItem</span></span>
<span data-ttu-id="6a2a0-144">A megadott katalógusegyesítési elem.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-144">The specified catalog item.</span></span>

### <span data-ttu-id="6a2a0-145">Lista<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="6a2a0-145">List<CatalogItem></span></span>
<span data-ttu-id="6a2a0-146">A megadott katalógusfájl listája a megfelelő tároló alatt.</span><span class="sxs-lookup"><span data-stu-id="6a2a0-146">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="6a2a0-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a2a0-147">NOTES</span></span>

## <span data-ttu-id="6a2a0-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a2a0-148">RELATED LINKS</span></span>

[<span data-ttu-id="6a2a0-149">Teszt-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="6a2a0-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


