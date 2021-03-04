---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 738820c4c06fd32862def36ec76983968e99efb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942818"
---
# <span data-ttu-id="dca09-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="dca09-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="dca09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca09-102">SYNOPSIS</span></span>
<span data-ttu-id="dca09-103">A Data Lake Analytics katalóguselemző elemét vagy elemtípusát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dca09-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="dca09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dca09-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dca09-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dca09-105">DESCRIPTION</span></span>
<span data-ttu-id="dca09-106">A **Get-AzDataLakeAnalyticsCatalogItem** kap egy megadott Azure Data Lake Analytics katalóguselemet, vagy egy megadott típusú katalógustételt.</span><span class="sxs-lookup"><span data-stu-id="dca09-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="dca09-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dca09-107">EXAMPLES</span></span>

### <span data-ttu-id="dca09-108">1. példa: Megadott adatbázis lekérte</span><span class="sxs-lookup"><span data-stu-id="dca09-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="dca09-109">Ez a parancs a megadott adatbázist kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dca09-109">This command gets the specified database.</span></span>

### <span data-ttu-id="dca09-110">2. példa: Táblák lekérte egy megadott adatbázisban és sémában</span><span class="sxs-lookup"><span data-stu-id="dca09-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="dca09-111">Ez a parancs lekérte a megadott adatbázis tábláinak listáját.</span><span class="sxs-lookup"><span data-stu-id="dca09-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="dca09-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dca09-112">PARAMETERS</span></span>

### <span data-ttu-id="dca09-113">-Account</span><span class="sxs-lookup"><span data-stu-id="dca09-113">-Account</span></span>
<span data-ttu-id="dca09-114">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca09-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="dca09-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca09-115">-DefaultProfile</span></span>
<span data-ttu-id="dca09-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dca09-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dca09-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="dca09-117">-ItemType</span></span>
<span data-ttu-id="dca09-118">A lehívni vagy felsorolni kívánt elem(ök) katalóguselemtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca09-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="dca09-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="dca09-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dca09-120">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="dca09-120">Database</span></span>
- <span data-ttu-id="dca09-121">Séma</span><span class="sxs-lookup"><span data-stu-id="dca09-121">Schema</span></span>
- <span data-ttu-id="dca09-122">Szerelvény</span><span class="sxs-lookup"><span data-stu-id="dca09-122">Assembly</span></span>
- <span data-ttu-id="dca09-123">Táblázat</span><span class="sxs-lookup"><span data-stu-id="dca09-123">Table</span></span>
- <span data-ttu-id="dca09-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="dca09-124">TableValuedFunction</span></span>
- <span data-ttu-id="dca09-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="dca09-125">TableStatistics</span></span>
- <span data-ttu-id="dca09-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="dca09-126">ExternalDataSource</span></span>
- <span data-ttu-id="dca09-127">Nézet</span><span class="sxs-lookup"><span data-stu-id="dca09-127">View</span></span>
- <span data-ttu-id="dca09-128">Eljárás</span><span class="sxs-lookup"><span data-stu-id="dca09-128">Procedure</span></span>
- <span data-ttu-id="dca09-129">Titkos</span><span class="sxs-lookup"><span data-stu-id="dca09-129">Secret</span></span>
- <span data-ttu-id="dca09-130">Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="dca09-130">Credential</span></span>
- <span data-ttu-id="dca09-131">Típusok</span><span class="sxs-lookup"><span data-stu-id="dca09-131">Types</span></span>
- <span data-ttu-id="dca09-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="dca09-132">TablePartition</span></span>

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

### <span data-ttu-id="dca09-133">-Path</span><span class="sxs-lookup"><span data-stu-id="dca09-133">-Path</span></span>
<span data-ttu-id="dca09-134">A visszakeresni kívánt elem vagy a listába sorolt elemek szülőelemének több részből álló elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca09-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="dca09-135">Az elérési út egyes részeit pont (.) választja el egymástól.</span><span class="sxs-lookup"><span data-stu-id="dca09-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="dca09-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca09-136">CommonParameters</span></span>
<span data-ttu-id="dca09-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca09-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca09-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca09-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca09-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dca09-139">INPUTS</span></span>

### <span data-ttu-id="dca09-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dca09-140">System.String</span></span>

### <span data-ttu-id="dca09-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="dca09-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="dca09-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="dca09-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="dca09-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca09-143">OUTPUTS</span></span>

### <span data-ttu-id="dca09-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="dca09-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="dca09-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dca09-145">NOTES</span></span>

## <span data-ttu-id="dca09-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dca09-146">RELATED LINKS</span></span>

[<span data-ttu-id="dca09-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="dca09-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


