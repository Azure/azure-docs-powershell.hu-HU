---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298121"
---
# <span data-ttu-id="065bd-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="065bd-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="065bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="065bd-102">SYNOPSIS</span></span>
<span data-ttu-id="065bd-103">Beolvassa az adattó-statisztika-katalógus elemeit vagy típusait.</span><span class="sxs-lookup"><span data-stu-id="065bd-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="065bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="065bd-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="065bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="065bd-105">DESCRIPTION</span></span>
<span data-ttu-id="065bd-106">A **Get-AzDataLakeAnalyticsCatalogItem** megkapja az Azure Data Lake-tó elemzési elemét, vagy egy megadott típusú katalógust kap.</span><span class="sxs-lookup"><span data-stu-id="065bd-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="065bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="065bd-107">EXAMPLES</span></span>

### <span data-ttu-id="065bd-108">Példa 1: megadott adatbázis beszerzése</span><span class="sxs-lookup"><span data-stu-id="065bd-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="065bd-109">Ez a parancs a megadott adatbázist kapja.</span><span class="sxs-lookup"><span data-stu-id="065bd-109">This command gets the specified database.</span></span>

### <span data-ttu-id="065bd-110">2. példa: táblázatok beszerzése egy megadott adatbázisban és sémában</span><span class="sxs-lookup"><span data-stu-id="065bd-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="065bd-111">Ez a parancs a megadott adatbázisban lévő táblák listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="065bd-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="065bd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="065bd-112">PARAMETERS</span></span>

### <span data-ttu-id="065bd-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="065bd-113">-Account</span></span>
<span data-ttu-id="065bd-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="065bd-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065bd-115">-DefaultProfile</span></span>
<span data-ttu-id="065bd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="065bd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="065bd-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="065bd-117">-ItemType</span></span>
<span data-ttu-id="065bd-118">A beolvasott vagy a listán szereplő elem (ek) katalógus-elemének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="065bd-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="065bd-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="065bd-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="065bd-120">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="065bd-120">Database</span></span>
- <span data-ttu-id="065bd-121">Séma</span><span class="sxs-lookup"><span data-stu-id="065bd-121">Schema</span></span>
- <span data-ttu-id="065bd-122">Összeállítási</span><span class="sxs-lookup"><span data-stu-id="065bd-122">Assembly</span></span>
- <span data-ttu-id="065bd-123">Táblázat</span><span class="sxs-lookup"><span data-stu-id="065bd-123">Table</span></span>
- <span data-ttu-id="065bd-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="065bd-124">TableValuedFunction</span></span>
- <span data-ttu-id="065bd-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="065bd-125">TableStatistics</span></span>
- <span data-ttu-id="065bd-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="065bd-126">ExternalDataSource</span></span>
- <span data-ttu-id="065bd-127">Nézd</span><span class="sxs-lookup"><span data-stu-id="065bd-127">View</span></span>
- <span data-ttu-id="065bd-128">Eljárás</span><span class="sxs-lookup"><span data-stu-id="065bd-128">Procedure</span></span>
- <span data-ttu-id="065bd-129">Titkos</span><span class="sxs-lookup"><span data-stu-id="065bd-129">Secret</span></span>
- <span data-ttu-id="065bd-130">Hitelesítőadat</span><span class="sxs-lookup"><span data-stu-id="065bd-130">Credential</span></span>
- <span data-ttu-id="065bd-131">Típusú</span><span class="sxs-lookup"><span data-stu-id="065bd-131">Types</span></span>
- <span data-ttu-id="065bd-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="065bd-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065bd-133">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="065bd-133">-Path</span></span>
<span data-ttu-id="065bd-134">A beolvasandó elem többrészes elérési útja vagy a lista elemeinek a fölérendelt eleme.</span><span class="sxs-lookup"><span data-stu-id="065bd-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="065bd-135">Az elérési út egyes részeit ponttal (.) kell elválasztani.</span><span class="sxs-lookup"><span data-stu-id="065bd-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065bd-136">CommonParameters</span></span>
<span data-ttu-id="065bd-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="065bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065bd-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="065bd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065bd-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="065bd-139">INPUTS</span></span>

### <span data-ttu-id="065bd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="065bd-140">System.String</span></span>

### <span data-ttu-id="065bd-141">Microsoft. Azure. Command. DataLakeAnalytics. modellek. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="065bd-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="065bd-142">Microsoft. Azure. Command. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="065bd-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="065bd-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="065bd-143">OUTPUTS</span></span>

### <span data-ttu-id="065bd-144">Microsoft. Azure. Management. DataLake. Analytics. models. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="065bd-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="065bd-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="065bd-145">NOTES</span></span>

## <span data-ttu-id="065bd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="065bd-146">RELATED LINKS</span></span>

[<span data-ttu-id="065bd-147">Teszt-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="065bd-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


