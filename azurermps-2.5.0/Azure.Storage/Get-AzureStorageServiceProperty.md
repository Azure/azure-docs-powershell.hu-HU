---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: adb671b81dd26c1fa66ea98f98dddf8fffbb5356
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848566"
---
# <span data-ttu-id="c9590-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c9590-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="c9590-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9590-102">SYNOPSIS</span></span>
<span data-ttu-id="c9590-103">Az Azure Storage Services tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="c9590-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9590-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9590-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9590-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9590-105">DESCRIPTION</span></span>
<span data-ttu-id="c9590-106">A **Get-AzureStorageServiceProperty** parancsmag az Azure Storage Services tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9590-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="c9590-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9590-107">EXAMPLES</span></span>

### <span data-ttu-id="c9590-108">Példa 1: az Azure Storage Services tulajdonság beszerzése a blob-szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="c9590-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29
```

<span data-ttu-id="c9590-109">Ez a parancs a Paca szolgáltatás DefaultServiceVersion tulajdonságát kapja.</span><span class="sxs-lookup"><span data-stu-id="c9590-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="c9590-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9590-110">PARAMETERS</span></span>

### <span data-ttu-id="c9590-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c9590-111">-Context</span></span>
<span data-ttu-id="c9590-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9590-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c9590-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c9590-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c9590-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9590-114">-DefaultProfile</span></span>
<span data-ttu-id="c9590-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9590-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9590-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c9590-116">-ServiceType</span></span>
<span data-ttu-id="c9590-117">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9590-117">Specifies the storage service type.</span></span>
<span data-ttu-id="c9590-118">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9590-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c9590-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c9590-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c9590-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="c9590-120">Blob</span></span> 
- <span data-ttu-id="c9590-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="c9590-121">Table</span></span>
- <span data-ttu-id="c9590-122">Várólista</span><span class="sxs-lookup"><span data-stu-id="c9590-122">Queue</span></span>
- <span data-ttu-id="c9590-123">Fájl</span><span class="sxs-lookup"><span data-stu-id="c9590-123">File</span></span>

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

### <span data-ttu-id="c9590-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9590-124">CommonParameters</span></span>
<span data-ttu-id="c9590-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9590-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9590-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9590-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9590-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9590-127">INPUTS</span></span>

### <span data-ttu-id="c9590-128">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9590-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c9590-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9590-129">OUTPUTS</span></span>

### <span data-ttu-id="c9590-130">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="c9590-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="c9590-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9590-131">NOTES</span></span>

## <span data-ttu-id="c9590-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9590-132">RELATED LINKS</span></span>
