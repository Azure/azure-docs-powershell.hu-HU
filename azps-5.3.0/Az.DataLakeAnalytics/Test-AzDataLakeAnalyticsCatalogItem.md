---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477005"
---
# <span data-ttu-id="ec76c-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="ec76c-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="ec76c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec76c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec76c-103">Azt ellenőrzi, hogy létezik-e katalóguselem.</span><span class="sxs-lookup"><span data-stu-id="ec76c-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="ec76c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec76c-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec76c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec76c-105">DESCRIPTION</span></span>
<span data-ttu-id="ec76c-106">A **Test-AzDataLakeAnalyticsCatalogItem** parancsmag ellenőrzi az Azure Data Lake Analytics katalóguselemző elem meglétét.</span><span class="sxs-lookup"><span data-stu-id="ec76c-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="ec76c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec76c-107">EXAMPLES</span></span>

### <span data-ttu-id="ec76c-108">1. példa: Katalóguselem létezik-e?</span><span class="sxs-lookup"><span data-stu-id="ec76c-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="ec76c-109">Ez a parancs azt teszteli, hogy létezik-e egy megadott sémaelem.</span><span class="sxs-lookup"><span data-stu-id="ec76c-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="ec76c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec76c-110">PARAMETERS</span></span>

### <span data-ttu-id="ec76c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="ec76c-111">-Account</span></span>
<span data-ttu-id="ec76c-112">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec76c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ec76c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec76c-113">-DefaultProfile</span></span>
<span data-ttu-id="ec76c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ec76c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec76c-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="ec76c-115">-ItemType</span></span>
<span data-ttu-id="ec76c-116">Az ellenőrizni kívánt elem katalóguselemtípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ec76c-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="ec76c-117">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ec76c-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec76c-118">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="ec76c-118">Database</span></span>
- <span data-ttu-id="ec76c-119">Séma</span><span class="sxs-lookup"><span data-stu-id="ec76c-119">Schema</span></span>
- <span data-ttu-id="ec76c-120">Szerelvény</span><span class="sxs-lookup"><span data-stu-id="ec76c-120">Assembly</span></span>
- <span data-ttu-id="ec76c-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="ec76c-121">Table</span></span>
- <span data-ttu-id="ec76c-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="ec76c-122">TablePartition</span></span>
- <span data-ttu-id="ec76c-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="ec76c-123">TableValuedFunction</span></span>
- <span data-ttu-id="ec76c-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="ec76c-124">TableStatistics</span></span>
- <span data-ttu-id="ec76c-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="ec76c-125">ExternalDataSource</span></span>
- <span data-ttu-id="ec76c-126">Nézet</span><span class="sxs-lookup"><span data-stu-id="ec76c-126">View</span></span>
- <span data-ttu-id="ec76c-127">Eljárás</span><span class="sxs-lookup"><span data-stu-id="ec76c-127">Procedure</span></span>
- <span data-ttu-id="ec76c-128">Titkos</span><span class="sxs-lookup"><span data-stu-id="ec76c-128">Secret</span></span>
- <span data-ttu-id="ec76c-129">Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ec76c-129">Credential</span></span>
- <span data-ttu-id="ec76c-130">Típusok</span><span class="sxs-lookup"><span data-stu-id="ec76c-130">Types</span></span>

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

### <span data-ttu-id="ec76c-131">-Path</span><span class="sxs-lookup"><span data-stu-id="ec76c-131">-Path</span></span>
<span data-ttu-id="ec76c-132">Megadja a lehívni kívánt elem vagy a listába sorolni kívánt elemek szülőelemének elérési útját.</span><span class="sxs-lookup"><span data-stu-id="ec76c-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec76c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec76c-133">CommonParameters</span></span>
<span data-ttu-id="ec76c-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec76c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec76c-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec76c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec76c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec76c-136">INPUTS</span></span>

### <span data-ttu-id="ec76c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ec76c-137">System.String</span></span>

### <span data-ttu-id="ec76c-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="ec76c-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="ec76c-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="ec76c-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="ec76c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec76c-140">OUTPUTS</span></span>

### <span data-ttu-id="ec76c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec76c-141">System.Boolean</span></span>

## <span data-ttu-id="ec76c-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec76c-142">NOTES</span></span>

## <span data-ttu-id="ec76c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec76c-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec76c-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="ec76c-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


