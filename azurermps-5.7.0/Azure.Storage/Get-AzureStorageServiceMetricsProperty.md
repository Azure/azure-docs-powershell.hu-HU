---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 9d7e8f5d69d2f0e570cd7ce7fb21b29eb7f11648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496756"
---
# <span data-ttu-id="98a34-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="98a34-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="98a34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98a34-102">SYNOPSIS</span></span>
<span data-ttu-id="98a34-103">Az Azure Storage szolgáltatás metrikájának tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="98a34-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98a34-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="98a34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98a34-105">DESCRIPTION</span></span>
<span data-ttu-id="98a34-106">A **Get-AzureStorageServiceMetricsProperty** parancsmag metrikák tulajdonságait az Azure Storage szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="98a34-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="98a34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98a34-107">EXAMPLES</span></span>

### <span data-ttu-id="98a34-108">1. példa: a blob-szolgáltatás metrikák tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="98a34-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="98a34-109">Ennek a parancsnak a metrikák típusa esetén a blob-tárolóra vonatkozó tulajdonságokat kell kinéznie.</span><span class="sxs-lookup"><span data-stu-id="98a34-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="98a34-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98a34-110">PARAMETERS</span></span>

### <span data-ttu-id="98a34-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="98a34-111">-Context</span></span>
<span data-ttu-id="98a34-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a34-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="98a34-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="98a34-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98a34-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="98a34-114">-MetricsType</span></span>
<span data-ttu-id="98a34-115">A mérőszám típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a34-115">Specifies a metrics type.</span></span>
<span data-ttu-id="98a34-116">Ez a parancsmag az Azure Storage Service metrikájának tulajdonságait adja meg a mérőszámok típusához, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="98a34-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="98a34-117">A paraméter elfogadható értékei a következők: óra és perc.</span><span class="sxs-lookup"><span data-stu-id="98a34-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a34-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="98a34-118">-ServiceType</span></span>
<span data-ttu-id="98a34-119">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a34-119">Specifies the storage service type.</span></span>
<span data-ttu-id="98a34-120">Ez a parancsmag a paraméter által megadott típus metrikájának tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a34-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="98a34-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="98a34-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98a34-122">BLOB</span><span class="sxs-lookup"><span data-stu-id="98a34-122">Blob</span></span> 
- <span data-ttu-id="98a34-123">Táblázat</span><span class="sxs-lookup"><span data-stu-id="98a34-123">Table</span></span>
- <span data-ttu-id="98a34-124">Várólista</span><span class="sxs-lookup"><span data-stu-id="98a34-124">Queue</span></span>
- <span data-ttu-id="98a34-125">Fájl</span><span class="sxs-lookup"><span data-stu-id="98a34-125">File</span></span> 

<span data-ttu-id="98a34-126">A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="98a34-126">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a34-127">CommonParameters</span></span>
<span data-ttu-id="98a34-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98a34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a34-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a34-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a34-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a34-130">INPUTS</span></span>

### <span data-ttu-id="98a34-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98a34-131">IStorageContext</span></span>

<span data-ttu-id="98a34-132">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="98a34-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="98a34-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a34-133">OUTPUTS</span></span>

### <span data-ttu-id="98a34-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="98a34-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="98a34-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98a34-135">NOTES</span></span>

## <span data-ttu-id="98a34-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98a34-136">RELATED LINKS</span></span>

[<span data-ttu-id="98a34-137">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="98a34-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="98a34-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="98a34-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


