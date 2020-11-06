---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: 28727ed903030c360b436edfac3d4cfb2a5d38ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496752"
---
# <span data-ttu-id="fd374-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fd374-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="fd374-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd374-102">SYNOPSIS</span></span>
<span data-ttu-id="fd374-103">Az Azure Storage Services tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="fd374-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd374-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd374-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd374-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd374-105">DESCRIPTION</span></span>
<span data-ttu-id="fd374-106">A **Get-AzureStorageServiceProperty** parancsmag az Azure Storage Services tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd374-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="fd374-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd374-107">EXAMPLES</span></span>

### <span data-ttu-id="fd374-108">Példa 1: az Azure Storage Services tulajdonság beszerzése a blob-szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="fd374-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="fd374-109">Ez a parancs a Paca szolgáltatás DefaultServiceVersion tulajdonságát kapja.</span><span class="sxs-lookup"><span data-stu-id="fd374-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="fd374-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd374-110">PARAMETERS</span></span>

### <span data-ttu-id="fd374-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fd374-111">-Context</span></span>
<span data-ttu-id="fd374-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd374-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fd374-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fd374-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd374-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fd374-114">-ServiceType</span></span>
<span data-ttu-id="fd374-115">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd374-115">Specifies the storage service type.</span></span>
<span data-ttu-id="fd374-116">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd374-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="fd374-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fd374-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd374-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="fd374-118">Blob</span></span> 
- <span data-ttu-id="fd374-119">Táblázat</span><span class="sxs-lookup"><span data-stu-id="fd374-119">Table</span></span>
- <span data-ttu-id="fd374-120">Várólista</span><span class="sxs-lookup"><span data-stu-id="fd374-120">Queue</span></span>
- <span data-ttu-id="fd374-121">Fájl</span><span class="sxs-lookup"><span data-stu-id="fd374-121">File</span></span>

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

### <span data-ttu-id="fd374-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd374-122">CommonParameters</span></span>
<span data-ttu-id="fd374-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd374-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd374-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd374-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd374-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd374-125">INPUTS</span></span>

### <span data-ttu-id="fd374-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd374-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fd374-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd374-127">OUTPUTS</span></span>

### <span data-ttu-id="fd374-128">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="fd374-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="fd374-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd374-129">NOTES</span></span>

## <span data-ttu-id="fd374-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd374-130">RELATED LINKS</span></span>

