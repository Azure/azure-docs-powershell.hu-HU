---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: fdd7a7c655b46eb3fc1ca8673fb8fb5f36dcd850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494250"
---
# <span data-ttu-id="b1a0e-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b1a0e-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="b1a0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a0e-103">Az Azure Storage szolgáltatás metrikájának tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="b1a0e-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1a0e-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a0e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1a0e-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a0e-106">A **Get-AzureStorageServiceMetricsProperty** parancsmag metrikák tulajdonságait az Azure Storage szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="b1a0e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1a0e-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a0e-108">1. példa: a blob-szolgáltatás metrikák tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="b1a0e-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="b1a0e-109">Ennek a parancsnak a metrikák típusa esetén a blob-tárolóra vonatkozó tulajdonságokat kell kinéznie.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="b1a0e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1a0e-110">PARAMETERS</span></span>

### <span data-ttu-id="b1a0e-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b1a0e-111">-Context</span></span>
<span data-ttu-id="b1a0e-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b1a0e-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a0e-114">-DefaultProfile</span></span>
<span data-ttu-id="b1a0e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0e-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="b1a0e-116">-MetricsType</span></span>
<span data-ttu-id="b1a0e-117">A mérőszám típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-117">Specifies a metrics type.</span></span>
<span data-ttu-id="b1a0e-118">Ez a parancsmag az Azure Storage Service metrikájának tulajdonságait adja meg a mérőszámok típusához, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="b1a0e-119">A paraméter elfogadható értékei a következők: óra és perc.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0e-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b1a0e-120">-ServiceType</span></span>
<span data-ttu-id="b1a0e-121">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-121">Specifies the storage service type.</span></span>
<span data-ttu-id="b1a0e-122">Ez a parancsmag a paraméter által megadott típus metrikájának tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="b1a0e-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b1a0e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1a0e-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="b1a0e-124">Blob</span></span> 
- <span data-ttu-id="b1a0e-125">Táblázat</span><span class="sxs-lookup"><span data-stu-id="b1a0e-125">Table</span></span>
- <span data-ttu-id="b1a0e-126">Várólista</span><span class="sxs-lookup"><span data-stu-id="b1a0e-126">Queue</span></span>
- <span data-ttu-id="b1a0e-127">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-127">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a0e-128">CommonParameters</span></span>
<span data-ttu-id="b1a0e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1a0e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a0e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a0e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a0e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1a0e-131">INPUTS</span></span>

### <span data-ttu-id="b1a0e-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b1a0e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b1a0e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1a0e-133">OUTPUTS</span></span>

### <span data-ttu-id="b1a0e-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="b1a0e-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="b1a0e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1a0e-135">NOTES</span></span>

## <span data-ttu-id="b1a0e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1a0e-136">RELATED LINKS</span></span>

[<span data-ttu-id="b1a0e-137">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b1a0e-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b1a0e-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b1a0e-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


