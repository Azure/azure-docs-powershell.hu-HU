---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: deb93fb17c2c739dcf377665f8b2f604a2fb4847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495387"
---
# <span data-ttu-id="efe09-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="efe09-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="efe09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efe09-102">SYNOPSIS</span></span>
<span data-ttu-id="efe09-103">A katalógusfájl létezésének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="efe09-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efe09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efe09-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efe09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="efe09-105">DESCRIPTION</span></span>
<span data-ttu-id="efe09-106">A **AzureRmDataLakeAnalyticsCatalogItem-** parancsmag ellenőrzi az Azure Data-tó elemzési katalógusának létezését.</span><span class="sxs-lookup"><span data-stu-id="efe09-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="efe09-107">Példák</span><span class="sxs-lookup"><span data-stu-id="efe09-107">EXAMPLES</span></span>

### <span data-ttu-id="efe09-108">1. példa: annak ellenőrzése, hogy létezik-e katalógus-elem</span><span class="sxs-lookup"><span data-stu-id="efe09-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="efe09-109">Ez a parancs azt teszteli, hogy létezik-e egy adott séma-elem.</span><span class="sxs-lookup"><span data-stu-id="efe09-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="efe09-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efe09-110">PARAMETERS</span></span>

### <span data-ttu-id="efe09-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="efe09-111">-Account</span></span>
<span data-ttu-id="efe09-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efe09-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="efe09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe09-113">-DefaultProfile</span></span>
<span data-ttu-id="efe09-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="efe09-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efe09-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="efe09-115">-ItemType</span></span>
<span data-ttu-id="efe09-116">Megadja az ellenőrizendő elem katalógus-elemének típusát.</span><span class="sxs-lookup"><span data-stu-id="efe09-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="efe09-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="efe09-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efe09-118">Adatbázis</span><span class="sxs-lookup"><span data-stu-id="efe09-118">Database</span></span>
- <span data-ttu-id="efe09-119">Séma</span><span class="sxs-lookup"><span data-stu-id="efe09-119">Schema</span></span>
- <span data-ttu-id="efe09-120">Összeállítási</span><span class="sxs-lookup"><span data-stu-id="efe09-120">Assembly</span></span>
- <span data-ttu-id="efe09-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="efe09-121">Table</span></span>
- <span data-ttu-id="efe09-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="efe09-122">TablePartition</span></span>
- <span data-ttu-id="efe09-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="efe09-123">TableValuedFunction</span></span>
- <span data-ttu-id="efe09-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="efe09-124">TableStatistics</span></span>
- <span data-ttu-id="efe09-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="efe09-125">ExternalDataSource</span></span>
- <span data-ttu-id="efe09-126">Nézd</span><span class="sxs-lookup"><span data-stu-id="efe09-126">View</span></span>
- <span data-ttu-id="efe09-127">Eljárás</span><span class="sxs-lookup"><span data-stu-id="efe09-127">Procedure</span></span>
- <span data-ttu-id="efe09-128">Titkos</span><span class="sxs-lookup"><span data-stu-id="efe09-128">Secret</span></span>
- <span data-ttu-id="efe09-129">Hitelesítőadat</span><span class="sxs-lookup"><span data-stu-id="efe09-129">Credential</span></span>
- <span data-ttu-id="efe09-130">Típusú</span><span class="sxs-lookup"><span data-stu-id="efe09-130">Types</span></span>

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

### <span data-ttu-id="efe09-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="efe09-131">-Path</span></span>
<span data-ttu-id="efe09-132">A beolvasni kívánt elem elérési útvonalát adja meg, vagy az elemek listájához tartozó fölérendelt elem elérési útját.</span><span class="sxs-lookup"><span data-stu-id="efe09-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe09-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe09-133">CommonParameters</span></span>
<span data-ttu-id="efe09-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efe09-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe09-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe09-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe09-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efe09-136">INPUTS</span></span>

### <span data-ttu-id="efe09-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="efe09-137">None</span></span>
<span data-ttu-id="efe09-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="efe09-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efe09-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efe09-139">OUTPUTS</span></span>

### <span data-ttu-id="efe09-140">bool</span><span class="sxs-lookup"><span data-stu-id="efe09-140">bool</span></span>
<span data-ttu-id="efe09-141">True vagy FALSE: azt jelzi, hogy a megadott katalógusfájl létezik-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="efe09-141">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="efe09-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efe09-142">NOTES</span></span>

## <span data-ttu-id="efe09-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efe09-143">RELATED LINKS</span></span>

[<span data-ttu-id="efe09-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="efe09-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


