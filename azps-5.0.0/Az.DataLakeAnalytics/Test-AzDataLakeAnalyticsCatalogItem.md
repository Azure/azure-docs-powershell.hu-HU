---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297974"
---
# <span data-ttu-id="08e66-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="08e66-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="08e66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08e66-102">SYNOPSIS</span></span>
<span data-ttu-id="08e66-103">A katalógusfájl létezésének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="08e66-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="08e66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08e66-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e66-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08e66-105">DESCRIPTION</span></span>
<span data-ttu-id="08e66-106">A **AzDataLakeAnalyticsCatalogItem-** parancsmag ellenőrzi az Azure Data-tó elemzési katalógusának létezését.</span><span class="sxs-lookup"><span data-stu-id="08e66-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="08e66-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08e66-107">EXAMPLES</span></span>

### <span data-ttu-id="08e66-108">1. példa: annak ellenőrzése, hogy létezik-e katalógus-elem</span><span class="sxs-lookup"><span data-stu-id="08e66-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="08e66-109">Ez a parancs azt teszteli, hogy létezik-e egy adott séma-elem.</span><span class="sxs-lookup"><span data-stu-id="08e66-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="08e66-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08e66-110">PARAMETERS</span></span>

### <span data-ttu-id="08e66-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="08e66-111">-Account</span></span>
<span data-ttu-id="08e66-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08e66-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="08e66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e66-113">-DefaultProfile</span></span>
<span data-ttu-id="08e66-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08e66-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08e66-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="08e66-115">-ItemType</span></span>
<span data-ttu-id="08e66-116">Megadja az ellenőrizendő elem katalógus-elemének típusát.</span><span class="sxs-lookup"><span data-stu-id="08e66-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="08e66-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="08e66-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08e66-118">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="08e66-118">Database</span></span>
- <span data-ttu-id="08e66-119">Séma</span><span class="sxs-lookup"><span data-stu-id="08e66-119">Schema</span></span>
- <span data-ttu-id="08e66-120">Összeállítási</span><span class="sxs-lookup"><span data-stu-id="08e66-120">Assembly</span></span>
- <span data-ttu-id="08e66-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="08e66-121">Table</span></span>
- <span data-ttu-id="08e66-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="08e66-122">TablePartition</span></span>
- <span data-ttu-id="08e66-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="08e66-123">TableValuedFunction</span></span>
- <span data-ttu-id="08e66-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="08e66-124">TableStatistics</span></span>
- <span data-ttu-id="08e66-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="08e66-125">ExternalDataSource</span></span>
- <span data-ttu-id="08e66-126">Nézd</span><span class="sxs-lookup"><span data-stu-id="08e66-126">View</span></span>
- <span data-ttu-id="08e66-127">Eljárás</span><span class="sxs-lookup"><span data-stu-id="08e66-127">Procedure</span></span>
- <span data-ttu-id="08e66-128">Titkos</span><span class="sxs-lookup"><span data-stu-id="08e66-128">Secret</span></span>
- <span data-ttu-id="08e66-129">Hitelesítőadat</span><span class="sxs-lookup"><span data-stu-id="08e66-129">Credential</span></span>
- <span data-ttu-id="08e66-130">Típusú</span><span class="sxs-lookup"><span data-stu-id="08e66-130">Types</span></span>

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

### <span data-ttu-id="08e66-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="08e66-131">-Path</span></span>
<span data-ttu-id="08e66-132">A beolvasni kívánt elem elérési útvonalát adja meg, vagy az elemek listájához tartozó fölérendelt elem elérési útját.</span><span class="sxs-lookup"><span data-stu-id="08e66-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="08e66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e66-133">CommonParameters</span></span>
<span data-ttu-id="08e66-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08e66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e66-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e66-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e66-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08e66-136">INPUTS</span></span>

### <span data-ttu-id="08e66-137">System. String</span><span class="sxs-lookup"><span data-stu-id="08e66-137">System.String</span></span>

### <span data-ttu-id="08e66-138">Microsoft. Azure. Command. DataLakeAnalytics. modellek. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="08e66-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="08e66-139">Microsoft. Azure. Command. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="08e66-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="08e66-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08e66-140">OUTPUTS</span></span>

### <span data-ttu-id="08e66-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08e66-141">System.Boolean</span></span>

## <span data-ttu-id="08e66-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08e66-142">NOTES</span></span>

## <span data-ttu-id="08e66-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08e66-143">RELATED LINKS</span></span>

[<span data-ttu-id="08e66-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="08e66-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


